## $\color{cyan}{\textsf{Kontrollieren}}$
| $\color{cyan}{\textsf{Arbeitspaket 5: Kontrollieren}}$ - Wurde der Auftrag korrekt umgesetzt?  |
| ---------------------------------------------------------------------------------------------- |
| Entscheiden anhand der ITSM Evaluation sowie Testing via Docker-Compose innerhalb der Umgebung |
Um meine Umgebung zu testen, wird der Server via Docker heruntergefahren.

Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden durch den Zabbix / Zendesk Webhook.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.
