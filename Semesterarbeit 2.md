# 1. Einführung
## 1.1 Beschreibung

In dieser Semesterarbeit möchte ich eine Evaluation von mind. 2 Ticketsystemen durchführen, das ausgewählte Ticketsystem anschliessend selbst hosten, dessen Benutzerzugänge sichern sowie ein System ausserhalb des Ticketsystems überwachen, welches bei Absturz einen automatischen Incident innerhalb des Ticketsystems auslöst. Hierbei möchte ich eine Kundenumgebung simulieren und die Theorie aus dem ITSM Modul in die Praxis umsetzen. 

Das Ticketsystem sollte kostenfrei und Benutzerfreundlich sein sowie Kompatibilität für self-hosting bieten.

## 1.2 IPERKA

### Informieren
Der erste Schritt ist der Evaluation der Ticketsysteme gewidmet.
Das Ticketsystem soll Funktionen beinhalten, welche im Alltäglichen Support sowie im ITIL-Prozess Grundlegend sind ***(Erstellen von Tickets / Incidents, Mailverkehr, Unterteilung von Agenten, Priorisierung von Incidents)***
Zudem muss das Ticket System die Möglichkeit bieten, es auf eigener Infrastruktur zu hosten.
So kann ich das System mit SEUSAG klar eingrenzen.
### Planen
Geplant wir anhand Arbeitspaketen, welche in den jeweiligen Sprint-Phasen ausgeführt werden.

Um die Übersicht zu behalten, werden diese Phasen sowie die Arbeitspakete in einem ***Gantt-Diagramm*** festgehalten.

.............................................
...........................................
...............................................

### Entscheiden
Entscheiden muss ich mich anhand folgenden Kriterien:

-
-
-
-
-
-
### Realisieren
Um Das Projekt zu realisieren wird eine Virtuelle Maschine (Virtueller Server) aufgesetzt. Diese Virtuelle Maschine simuliert eine Betriebsrelevante Maschine welche ohne Downtime aktiv bleibt.
### Kontrollieren
Um meine Umgebung zu testen, wird der Server manuell heruntergefahren.
Sobald der Server nicht mehr erreichbar ist, muss automatisch ein Ticket ausgelöst werden welches im ausgewählten Ticketsystem erscheinen muss.

Dieses Ticket kann einen Text beinhalten welches die nötigsten Informationen zum betroffenen System beinhaltet um anhand den Informationen allfällig Troubleshooting betreiben kann.
### Auswerten
Die Auswertung findet mit dem Resultat des K im IPERKA (Kontrollieren) statt.
Wenn das Ticket die korrekte Information wiedergibt und unmittelbar nach der Downtime des Servers generiert wird und auf dem Dashboard der Ticketsystems erscheint, gilt die Auswertung als erfolgreich.