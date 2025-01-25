## $\color{red}{\textsf{Informieren}}$

| $\color{red}{\textsf{Arbeitspaket 1: Informieren}}$ - Was genau beinhaltet der Auftrag? |
| --------------------------------------------------------------------------------------- |
| Brainstorming/Online-Suche, Prüfkriterien definieren, Sachmittel aussuchen              |

### :mag: 1. Recherche; Brainstorming/Online-Suche

Zuerst habe ich mich online über Ticket-System Lösungen informiert, welche self-hosting unterstützen und essentielle ITSM-Funktionen nach ITIL beinhalten.

Die Kriterien
- Monitoringkompatibilität und einfache Integration der Monitoring-Funktionalitäten
- Self-Hosting und Orchestrierung (Dabei ist die Kompatibilität mit Docker-Compose wichtig) -> Klare Eingrenzung via SEUSAG
- Kostenloser Zugriff / Freie Lizenz
waren ebenfalls Bestandteil meiner Recherche.

*Folgende Lösungen habe ich in den Google-Suchergebnissen gefunden sowie von Benutzerempfehlungen auf Reddit.com:

| Potentielle Ticketsysteme aus meiner Online-Suche sind |
| ------------------------------------------------------ |
| -  OTRS                                                |
| - ZAMMAD                                               |
| - FREESCOUT                                            |

| Potentielle Monitoring-Lösungen aus meiner Online Suche |
| ------------------------------------------------------- |
| -  PASSLERS PRTG                                        |
| - ZABBIX MONITORING                                     |

### :scroll: 2. Prüfkriterien definieren

- Die Prüfkriterien für die Evaluation habe ich aus dem ITIL v4 Framework ausgesucht.
![](../_attachments/3_ITSM_Grundlagen.png)

Um eine präzisere Evaluation zu gewährleisten, habe ich innerhalb der Prüfkriterien, Kernkriterien hinzugefügt welche mit dem ITIL Framework korrelieren:

| ITSM-Funktion              | Kernfunktionen                              |
| -------------------------- | ------------------------------------------- |
| Incident Management        | Tickets, SLAs, Workflows, Multi-Channel     |
| Change Management          | Change-Tickets, Genehmigungen, Risikofelder |
| Problem Management         | Problem-Tickets, Incident-Linking, RCA      |
| Knowledge Management       | KB, Kategorien, Suche, Versionen            |
| IT Asset Management        | Asset-Tracking, Linking, Custom Fields      |
| Service Desk               | Multi-Channel, Portal, Routing, Tools       |
| Service Catalog            | Request-Forms, Kategorien, Portal           |
| Service Request Management | Formulare, Workflows, Genehmigungen         |

Damit Kommunikation innerhalb der Docker-Netzwerkstruktur und den Schnittstellen der potentiellen Lösungen funktionieren kann, habe ich zudem zusätzliche Evaluationskriterien definiert:

| Weitere Evaluationskriterien: |                                                                          |
| ----------------------------- | ------------------------------------------------------------------------ |
| - Docker-Kompatibilität       | Für Kompatibilität mit meiner Orchestrierung                             |
| - Agenten-Unterteilung        | Verschiedene ITSM-Agenten für verschiedene Prozesse und Zwecke erstellen |
| - Workflows                   | Für Automationsprozesse                                                  |
| - API-Funktionalität          | API-Zugriffe für ITSM und Monitoring                                     |

*Die vollumfängliche Evaluation ist unter IPERKA-SCHRITT PLANEN ersichtlich
- [MATRIX](../2_Planen/ITSM_Evaluation_Ticketsysteme.md)

### :wrench: 3. Sachmittel aussuchen

Bei den Sachmittel für die Umsetzung habe ich mich an eine Cloud-Native Lösung Orientiert. Dabei habe ich mir **Docker** ausgesucht, da Docker während unserer Weiterbildung im Modul zum Cloud-Native Engineer eingesetzt wird.
______
