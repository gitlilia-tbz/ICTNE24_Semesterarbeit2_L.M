## 1.2 IPERKA


### $\color{red}{\textsf{Arbeitspaket 1}}$

| $\color{red}{\textsf{Arbeitspaket 1: Informieren}}$                              |
| -------------------------------------------------------------------------------- |
| Brainstorming/Online-Suche, Auswahl-Kriterien Definieren, Evaluation durchführen |

#### :mag: Brainstorming/Online-Suche

Zuerst habe ich mich online über Ticket-System Lösungen informiert, welche self-hosting unterstützen und essentielle ITSM-Funktionen beinhalten.


- Monitoringkompatibilität und einfache Integration der Monitoring-Funktionalitäten
- *****Scalability /  Orchestrierung
- Ticketing-Funktionalität
- Kostenloser Zugriff / Freie Lizenz


Das Ticketsystem soll Funktionen beinhalten, welche im Alltäglichen Support sowie im ITIL-Prozess Grundlegend sind ***(Erstellen von Tickets / Incidents, Mailverkehr, Unterteilung von Agenten, Priorisierung von Incidents)***
Zudem muss das Ticket System die Möglichkeit bieten, es auf eigener Infrastruktur zu hosten.


So kann ich das System mit SEUSAG klar eingrenzen.

	LINK ZUR EVALUATION
### $\color{orange}{\textsf{ Arbeitspaket 2: Planen}}$

Geplant wir anhand Arbeitspaketen, welche in den jeweiligen Sprint-Phasen ausgeführt werden.

Um die Übersicht zu behalten, werden diese Phasen sowie die Arbeitspakete in einem ***Gantt-Diagramm*** festgehalten.

.............................................
...........................................
...............................................

#### Arbeits Pakete

...

#### Sprint-Phasen
...

#### Gantt-Diagramm
...

### ### $\color{yellow}{\textsf{ Arbeitspaket 3: Entscheiden}}$

-
Nach Tests innerhalb meiner Docker-Umgebung habe ich mich für folgende Lösung entschieden
- Zabbix Monitoring 
Kandidaten welche ausgeschieden wurden waren PRTG sowie Service-NOW
- Docker 
Für eine Plattform welche dem Lehrgang gerecht ist und höchste Flexibilität zur Orchestrierung der Lösung. iAC
- Zendesk Helpdesk
Für die Rasche
-
-
-


### $\color{lime}{\textsf{ Arbeitspaket 4: Realisieren}}$ 

1. Docker-Compose Files einrichten

Die Realisierung des Projektes 
#### SEUSAG Übersicht
.....


##### SEUSAG - Beschreibung

### $\color{cyan}{\textsf{ Arbeitspaket 5: Kontrollieren}}$ 
Um meine Umgebung zu testen, wird der Server via Docker heruntergefahren.

Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden durch den Zabbix / Zendesk Webhook.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.
### $\color{purple}{\textsf{ Arbeitspaket 6: Auswerten}}$ 
Die Auswertung findet mit dem Resultat des K im IPERKA (Kontrollieren) statt.
Wenn das Ticket die korrekte Information wiedergibt und unmittelbar nach der Downtime des Servers generiert wird und auf dem Dashboard der Ticketsystems erscheint, gilt die Auswertung als erfolgreich.
