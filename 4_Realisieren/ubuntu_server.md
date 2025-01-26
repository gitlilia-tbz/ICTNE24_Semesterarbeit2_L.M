## 1. Beschreibung Ubuntu (Server Lilia GMBH) - Testkunde
| 🤖 Disclamer: Dieser Code wurde durch Claude-AI gestützt                   |
| -------------------------------------------------------------------------- |
| [Siehe diesen Link für weitere Informationen](../Quellen_und_Disclamer.md) |

Das Ubuntu-Server-YAML konfiguriert einen einzelnen Zabbix-Agent-Container:

- Basiert auf Zabbix-Agent 6.4 (Ubuntu)
- Läuft auf Port 10055 (extern) / 10050 (intern)
- Nutzt das bestehende Zabbix-Netzwerk mit IP 172.20.0.6
- Debug-Level 4 für detaillierte Logs
- Erlaubt aktives und passives Monitoring
- Verbindet sich mit dem Zabbix-Server über Port 10051
---

Im Docker-Compose File des Ubuntu Server wird die Zugehörigkeit zum zabbix-net Netzwerk beschrieben. Zudem wird ein Zabbix-Agent installiert. Der Zabbix Agent dient zur Verbindung zum Zabbix Server.

```yaml
version: '3.8'

services:

  ubuntu-server:

    image: zabbix/zabbix-agent:ubuntu-6.4-latest

    container_name: ubuntu-server

    hostname: ubuntu-server

    restart: unless-stopped

    privileged: true

    mac_address: 02:42:ac:14:00:06

    ports:

      - "10055:10050"

    environment:

      - ZBX_HOSTNAME=ubuntu-server

      - ZBX_SERVER_HOST=zabbix-server

      - ZBX_SERVER_PORT=10051

      - ZBX_PASSIVE_ALLOW=true

      - ZBX_ACTIVE_ALLOW=true

      - ZBX_DEBUGLEVEL=4

    networks:

      zabbix-net:

        ipv4_address: 172.20.0.6

  

networks:

  zabbix-net:

    external: true

    name: zabbix_server_70_zabbix-net
```