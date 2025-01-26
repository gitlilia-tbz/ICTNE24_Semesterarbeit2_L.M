## $\color{cyan}{\textsf{Kontrollieren}}$
| $\color{cyan}{\textsf{Arbeitspaket 5: Kontrollieren}}$ - Wurde der Auftrag korrekt umgesetzt? |
| --------------------------------------------------------------------------------------------- |
| Testing der Umgebung                                                                          |
### 1. Kontrolle der folgenden Punkte:

#### - Aktivität der Services

Damit ich sicherstellen kann, das alle Elemente des Monitoring funktionieren muss ich kontrollieren, ob alle Docker Aktiv sind und die einzelnen Services keine Error-Messages generieren:

Aktivität des Ubuntu Server (Monitoring Target):
- Zabbix Agent OK
![](7_ubuntu_OK.png)


Aktivität des Zabbix Monitoring:

![](5_zabbix_OK.png)
nginx: OK
Agent: OK
Server: OK
mysql Datenbank: ok

Aktivität des Zammad ITSM:

![[4_zammad_ok.png]]
- Websocket: OK
- nginx: OK
- Scheduler: Aktiv
- Zammad-Init: Complete
- Railsserver: OK
- Elasticsearch: OK
- Redis: OK
- Postgresql: OK



Zammad sowie Zabbix sind via WebGUI erreichbar
____

#### - Connectivity

Um die Connectivity in meinem Docker-Netzwerk zu testen, werde ich alle Mitglieder gegenseitig anpingen und auf die einzelnen Web-Interfaces zugreifen:

Ping Ubuntu -> Zabbix ![[6_ping_server_zu_zabbix.png]]

Ping Zabbix->zammad

Ping Zabbix->ubuntu

Ping Zammad->Zabbix

Ping Zammad->ubuntu

___

#### - Persistenz
Zabbix:
- ✓ Sicher - Alle Daten (MySQL, Server-Konfiguration, Server-Daten) werden in persistenten Volumes gespeichert
```yaml
volumes:
  - zabbix-server-data:/var/lib/zabbix
  - zabbix-server-conf:/etc/zabbix

volumes:
  zabbix-server-data:
    driver: local
  zabbix-server-conf:
    driver: local
```

Zammad:
- ✓ Sicher - Alle kritischen Daten (PostgreSQL, Elasticsearch, Anwendungsdaten, Backups) nutzen persistente Volumes
```yaml
volumes:
  - zammad-data:/opt/zammad
  - zammad-backup:/var/tmp/zammad

volumes:
  postgres-data:
  elasticsearch-data:
  zammad-data:
  zammad-backup:
```

Ubuntu Server:
- ✓ Sicher - Keine persistenten Daten zu verlieren, nur Konfiguration in der Compose-Datei. Fixe IP-Adresse und MAC-Adresse definiert.
```yaml

    mac_address: 02:42:ac:14:00:06
    
# und fixe IP-Adresse

    networks:

      zabbix-net:

        ipv4_address: 172.20.0.6
```

Die Volumes bleiben nach `docker compose down` erhalten. Sie werden jedoch gelöscht, wenn ich`docker compose down -v` verwende.

Um die Persistenz vollständig auf ihre härte zu testen, werde ich die Konfiguration Abschliessen, alle Monitoring Elemente via `docker compose down` herunternehmen und anschliessend via `docker compose up` wieder initialisieren und herauffahren.

Die Container dürfen bei einem Erfolgreichen Resultat ihre Konfiguration nicht verlieren:



____


#### - Auslösen des Alarms
Um meine Umgebung zu testen, wird der Server via Docker heruntergefahren.

Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden durch den Zabbix / Zendesk Webhook.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.

- Generieren des Tickets

