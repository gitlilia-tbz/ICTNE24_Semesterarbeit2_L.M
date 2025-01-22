# Umsetzung / IPERKA

## $\color{red}{\textsf{Informieren}}$

| $\color{red}{\textsf{Arbeitspaket 1: Informieren}}$ - Was genau beinhaltet der Auftrag? |
| --------------------------------------------------------------------------------------- |
| Brainstorming/Online-Suche, Prüfkriterien definieren, Sachmittel aussuchen              |

#### :mag: Brainstorming/Online-Suche

Zuerst habe ich mich online über Ticket-System Lösungen informiert, welche self-hosting unterstützen und essentielle ITSM-Funktionen beinhalten.

- Monitoringkompatibilität und einfache Integration der Monitoring-Funktionalitäten
- Orchestrierung (Dabei ist die Kompatibilität mit Docker-Compose wichtig)
- Ticketing-Funktionalität
- Kostenloser Zugriff / Freie Lizenz

Das Ticketsystem soll Funktionen beinhalten, welche im Alltäglichen Support sowie im ITIL-Prozess Grundlegend sind. Diese sind unten in den definierten Prüfkriterien ersichtlich.
Zudem muss das Ticket System die Möglichkeit bieten, es auf eigener Infrastruktur zu hosten.
So kann ich das System mit SEUSAG klar eingrenzen.

Potentielle Ticketsysteme aus meiner Online-Suche

- OTRS
- ZAMMAD
- FREESCOUT

Potentielle Monitoring-Lösungen aus meiner Online Suche
- Paesslers PRTG
- Zabbix

#### :scroll: Prüfkriterien definieren

- Die Prüfkriterien für die Evaluation habe ich aus dem ITIL v4 Framework ausgesucht.
![](3_ITSM_Grundlagen.png)


#### :wrench: Sachmittel aussuchen

Bei den Sachmittel für die Umsetzung habe ich mich an eine Cloud-Native Lösung Orientiert. Dabei habe ich mir **Docker** ausgesucht.
______

## $\color{orange}{\textsf{Planen}}$

| $\color{orange}{\textsf{Arbeitspaket 2: Planen}}$ - Welche Lösungsmöglichkeiten sind vorhanden?           |
| --------------------------------------------------------------------------------------------------------- |
| Evaluation mit den Prüfkriterien aufbauen, Testing definieren, Risiken abschätzen sowie Zeitliche Planung |
- [SPRINT-GANTT und SEUSAG](.Sprint_und_GANTT)
- Risikodefinition

Geplant wird anhand der definierten Arbeitspakete, welche in den jeweiligen Sprint-Phasen ausgeführt werden und in der Umsetzung beschrieben sind.

Um die zeitliche Übersicht zu behalten, werden diese Phasen sowie die Arbeitspakete in einem ***Gantt-Diagramm*** festgehalten.

| :pushpin: Link zur Evaluation:                                       |
| -------------------------------------------------------------------- |
| [ITSM Evaluation der Ticketsysteme](./ITSM_Evaluation_Ticketsysteme) |

LINK ZU SPRINT UND GANNT
___
## $\color{yellow}{\textsf{Entscheiden}}$

| $\color{yellow}{\textsf{Arbeitspaket 3: Entscheiden}}$ - Welcher Lösungsweg wird eingeschlagen? |
| ----------------------------------------------------------------------------------------------- |
| Evaluation anhand der Prüfkriterien durchführen, Lösungsvariante wählen                         |
Nach Tests innerhalb meiner Docker-Umgebung habe ich mich definitiv für folgende Lösung entschieden
- Zabbix Monitoring 
Kandidaten welche ausgeschieden wurden waren PRTG sowie Service-NOW
- Docker 
Für eine Plattform welche dem Lehrgang gerecht ist und höchste Flexibilität zur Orchestrierung der Lösung. iAC
- Zendesk Helpdesk
Für die Rasche

___
## $\color{lime}{\textsf{Realisieren}}$ 

| $\color{lime}{\textsf{Arbeitspaket 4: Realisieren}}$ - Worauf muss bei der Umsetzung geachtet werden? |
| ----------------------------------------------------------------------------------------------------- |
| Umsetzung und Dokumentation, Arbeit nach Checkliste                                                   |

1. Docker-Compose Files einrichten

Die Realisierung des Projektes 
#### SEUSAG Übersicht
.....


##### SEUSAG - Beschreibung

___

## $\color{cyan}{\textsf{Kontrollieren}}$
| $\color{cyan}{\textsf{Arbeitspaket 5: Kontrollieren}}$ - Wurde der Auftrag korrekt umgesetzt?  |
| ---------------------------------------------------------------------------------------------- |
| Entscheiden anhand der ITSM Evaluation sowie Testing via Docker-Compose innerhalb der Umgebung |
Um meine Umgebung zu testen, wird der Server via Docker heruntergefahren.

Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden durch den Zabbix / Zendesk Webhook.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.
## $\color{purple}{\textsf{Auswerten}}$ 
| $\color{Purple}{\textsf{Arbeitspaket 6: Auswerten}}$ - Was gelang gut, was weniger? |
| ----------------------------------------------------------------------------------- |
| Reflexion und Fazit                                                                 |
[Reflexion](./Reflexion)
___
