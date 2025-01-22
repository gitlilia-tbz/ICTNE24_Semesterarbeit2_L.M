# Realisation

Technische Umsetzung:
## Docker-Composefiles

- Docker Compose Zabbix

- Docker Compose Ubuntu Server
- Docker Compose Zammad

Compose-Errors beseitigen

___
### Server OK
- Zabbix Agent OK
![[7_ubuntu_OK.png]]

### Monitoring OK
![[5_zabbix_OK.png]]
### Ticketsystem: OK
![[4_zammad_ok.png]]
- Websocket: OK
- nginx: OK
- Scheduler: Aktiv
- Zammad-Init: Complete
- Railsserver: OK
- Elasticsearch: OK
- Redis: OK
- Postgresql: OK

___
## Docker-Check

Docker-Environment steht.

Monitoring Implementiert

Ticketsystem Implementiert

Test-Ubuntu-Server Implementiert
___
## Connectivity Check

Ping Ubuntu -> Zabbix ![[6_ping_server_zu_zabbix.png]]

Ping Zabbix->zammad

Ping Zabbix->ubuntu

Ping Zammad->Zabbix

Ping Zammad->ubuntu
___
## Alerting via Webhook zu Zammad

API Token erstellt

Alerting User für Zammad

API im Zabbix implementiert

Action hinzugefügt

Sendung des Tickets