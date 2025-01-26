# Risikodefinition

In diesem Abschnitt wird die Risikodefinition beschrieben. Diese Risikodefinitionen beschreiben allfällige Risiken welche innerhalb meiner Projektarbeit auftreten könnten und wie diesen Risiken entgegengespielt werden.

:triangular_flag_on_post: 1. Kompatibilität und Funktionsabdeckung
Fehlende Kompatibilität der Monitoring und ITSM Lösung

:white_check_mark: Gegenmassname: Ausführliche Evaluation des ITSM-Systems mit Evaluationsmatrix sowie Testing mit der Monitoring Lösung innerhalb Docker (Docker-Compose, Netzwerkerreichbarkeit und API-Implementation zwischen ITSM und Monitoring)
____
:triangular_flag_on_post: 2. Stabilität (Synchro zwischen Server und Agent) und Zuverlässigkeit der Alerting

:white_check_mark: Gegenmassname:
- Service-Abdeckung innerhalb der Docker-Compose Files (Sicherstellen, das alle nötigen Services im Docker-Compose die richtigen Docker-Container bereitstellen) sowie System-Logs beobachten und ping-Tests zwischen Server und Agenten ausführen.
- Fixe IP Adressierung im Netz und korrekte Port-Zuteilung
- Persistente Docker Configuration
____
:triangular_flag_on_post: 3. Zeiteinhaltung

:white_check_mark: Gegenmassname:
Planung des Projektes in einzelne Arbeitsschritte / Arbeitspakete, Planung des Projektes via Gantt Diagramm und Checklisten erarbeiten.
___
:triangular_flag_on_post: 4. Sicherung der Daten / Datenverlust / Persistenz der Cloud-Umgebung

:white_check_mark: Gegenmassname:
- Codebase-Backup im Github ablegen und Bilder zur Dokumentation im persönlichen OneDrive sichern.
- Dokumentation regelmässig im Github sichern.
- Files persistent schreiben. Beim Herunterfahren der Systeme darf kein Datenverlust stattfinden -> Daher Files persistent schreiben, das Volumes gesichert werden und Systeme bewusst herunterfahren ohne Volumes zu löschen
	Docker-compose down anstatt Docker-compose down -v (-V löscht alle dazugehörigen Volumes)
____
