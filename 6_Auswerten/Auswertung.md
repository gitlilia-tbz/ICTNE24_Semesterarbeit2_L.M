# Auswertung

## :green_book: - Sind alle Ziele erreicht worden?
| :checkered_flag: Ziele                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------------- |
| - Das Ticketsystem erfolgreich implementieren und Betriebsbereit machen :white_check_mark:                                 |
| - Das Ticketsystem muss mit den definieren Benutzerzugängen für die Kundensimulation erreichbar sein.   :white_check_mark: |
| - Bei Absturz des zu überwachenden Systems muss automatisch ein Ticket generiert werden :white_check_mark:                 |

- Das Ticketsystem erfolgreich implementieren und Betriebsbereit machen :white_check_mark:
![](../_attachments/41_auswertung_zammad.png)
---

- Das Ticketsystem muss mit den definieren Benutzerzugängen für die Kundensimulation erreichbar sein.   :white_check_mark:
![](../_attachments/46_auswertung_benutzer.png)

- User zammad@liliagmbh ist der Ticket-Agent / Bot User , welcher den Ticket-Trigger verarbeitet.
- User james@liliagmbh ist der allgemeine Administrator der Umgebung..
(Alle Benutzerzugänge für die Kundensimulation sind separat in einem Passwortsafe abgelegt)

---

- Bei Absturz des zu überwachenden Systems muss automatisch ein Ticket generiert werden :white_check_mark:
![](../_attachments/10_zabbix_sent_green.png)
-> Ticket-Trigger via Webhook gesendet

---

![](../_attachments/11_zammad_ticket_ok.png)
-> Generiertes Ticket innerhalb Zammad

---
Docker-Container:

- Zabbix Container:

![](../_attachments/42_auswertung_docker_zabbix.png)
Alle Online und erreichbar :white_check_mark:


- Zammad-Container:

![](../_attachments/43_auswertung_docker_zammad.png)
Alle online und erreichbar, zammad-init ohne Fehler durchgeführt :white_check_mark:

- Ubuntu-Container:

![](../_attachments/44_auswertung_docker_ubuntu_server.png)
Ubuntu-Server mit Zabbix Agent aktiv. :white_check_mark:


- Gesamte Docker-Struktur:
![](../_attachments/45_auswertung_docker_all.png)
Alle Container online und erreichbar :white_check_mark:

:white_check_mark: Ja, alle Ziele, die ich am Anfang des Projektes definiert habe, wurden in meinem Projekt erreicht. Zudem konnte 3 anstatt wie in der Projektbeschreibung "mind. 2" ITSM Lösungen evaluieren. Projekt wurde übertroffen.
