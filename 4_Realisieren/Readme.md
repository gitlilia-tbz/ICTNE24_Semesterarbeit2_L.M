## $\color{lime}{\textsf{Realisieren}}$ 

| $\color{lime}{\textsf{Arbeitspaket 4: Realisieren}}$ - Worauf muss bei der Umsetzung geachtet werden? |
| ----------------------------------------------------------------------------------------------------- |
| Umsetzung und Dokumentation, Arbeit nach Checkliste                                                   |
### 1. Docker-Compose Files einrichten

- Ordnerstruktur erstellen
- Docker-Compose Files erstellen: Zammad, Zabbix und Ubuntu Test-Server (Lilia GMBH)


## Wie wird der API Webhook Realisiert?

Technische Quelle:
https://www.zabbix.com/de/integrations/zammad

1. In Zammad:
   - API Token-Zugriff aktivieren unter Einstellungen > System > API
   - Neuen Benutzer für Zabbix erstellen mit E-Mail
   - Persönliches Token mit ticket.agent-Berechtigung generieren

2. In Zabbix:
   - Globale Makro {$ZABBIX.URL} mit Frontend-URL erstellen
   - media_zammad.yaml importieren unter Administration > Medientypen
   - Zammad Medientyp konfigurieren:
     * zammad_access_token = Persönliches Token
     * zammad_url = Zammad Frontend-URL
     * zammad_customer = Zammad Benutzer-Email
     * zammad_enable_tags = true/false
     * Optional: Severity-Mapping via severity_(In diesem Beispiel - Severity HIGH)

3. Zabbix-Benutzer im Zabbix erstellen:
   - Media vom Typ Zammad hinzufügen
   - Beliebigen Text bei "Send to" eingeben


## 2. Ubuntu Server Einrichten
 [Alle Schritte Ubuntu Server](ubuntu_server.md)

## 3. Zammad Einrichten
 [Alle Schritte Zammad ITSM](zammad.md)

## 4. Zabbix Einrichten
 [Alle Schritte Zabbix Monitoring](zabbix.md)


### 5. Netzwerk / Zugriffsübersicht
 [SEUSAG / Netzwerkübersicht](SEUSAG_Netzwerkübersicht.md)

___
