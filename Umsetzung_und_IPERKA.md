## 1.2 IPERKA

### $\color{red}{\textsf{Informieren}}$

| $\color{red}{\textsf{Arbeitspaket 1: Informieren}}$ - Was genau beinhaltet der Auftrag? |
| --------------------------------------------------------------------------------------- |
| Brainstorming/Online-Suche, Prüfkriterien definieren, Sachmittel aussuchen              |

#### :mag: Brainstorming/Online-Suche

	Zuerst habe ich mich online über Ticket-System Lösungen informiert, welche self-hosting unterstützen und essentielle ITSM-Funktionen beinhalten.


- Monitoringkompatibilität und einfache Integration der Monitoring-Funktionalitäten
- Orchestrierung (Dabei ist die Kompatibilität mit Docker-Compose wichtig)
- Ticketing-Funktionalität
- Kostenloser Zugriff / Freie Lizenz

Das Ticketsystem soll Funktionen beinhalten, welche im Alltäglichen Support sowie im ITIL-Prozess Grundlegend sind.
Zudem muss das Ticket System die Möglichkeit bieten, es auf eigener Infrastruktur zu hosten.
So kann ich das System mit SEUSAG klar eingrenzen.


### $\color{orange}{\textsf{Planen}}$

| $\color{orange}{\textsf{Arbeitspaket 2: Planen}}$ - Welche Lösungsmöglichkeiten sind vorhanden?           |
| --------------------------------------------------------------------------------------------------------- |
| Evaluation mit den Prüfkriterien aufbauen, Testing definieren, Risiken abschätzen sowie Zeitliche Planung |
- Arbeitspakete definieren
- [SPRINT-GANTT und SEUSAG](.Sprint_und_GANTT)

Geplant wird anhand der definierten Arbeitspakete, welche in den jeweiligen Sprint-Phasen ausgeführt werden und in der Umsetzung beschrieben sind.

Um die zeitliche Übersicht zu behalten, werden diese Phasen sowie die Arbeitspakete in einem ***Gantt-Diagramm*** festgehalten.
Um die 

| :pushpin: Link zur Evaluation:                                       |
| -------------------------------------------------------------------- |
| [ITSM Evaluation der Ticketsysteme](./ITSM_Evaluation_Ticketsysteme) |

LINK ZU SPRINT UND GANNT
### $\color{yellow}{\textsf{ Arbeitspaket 3: Entscheiden}}$

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

### $\color{lime}{\textsf{ Arbeitspaket 4: Realisieren}}$ 

| $\color{lime}{\textsf{Arbeitspaket 4: Realisieren}}$ - Worauf muss bei der Umsetzung geachtet werden? |
| ----------------------------------------------------------------------------------------------------- |
| Umsetzung und Dokumentation, Arbeit nach Checkliste                                                   |

1. Docker-Compose Files einrichten

Die Realisierung des Projektes 
#### SEUSAG Übersicht
.....


##### SEUSAG - Beschreibung

### $\color{cyan}{\textsf{ Arbeitspaket 5: Kontrollieren}}$
| $\color{cyan}{\textsf{Arbeitspaket 5: Kontrollieren}}$ - Wurde der Auftrag korrekt umgesetzt?  |
| ---------------------------------------------------------------------------------------------- |
| Entscheiden anhand der ITSM Evaluation sowie Testing via Docker-Compose innerhalb der Umgebung |
Um meine Umgebung zu testen, wird der Server via Docker heruntergefahren.

Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden durch den Zabbix / Zendesk Webhook.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.
### $\color{purple}{\textsf{ Arbeitspaket 6: Auswerten}}$ 
| $\color{Purple}{\textsf{Arbeitspaket 6: Auswerten}}$ - Was gelang gut, was weniger? |
| ----------------------------------------------------------------------------------- |
| Arbeitspakete definieren, SPRINT und GANTT sowie SEUSAG-Skizze                      |
Die Auswertung findet mit dem Resultat des K im IPERKA (Kontrollieren) statt.
Wenn das Ticket die korrekte Information wiedergibt und unmittelbar nach der Downtime des Servers generiert wird und auf dem Dashboard der Ticketsystems erscheint, gilt die Auswertung als erfolgreich.

[Reflexion](./Reflexion)
