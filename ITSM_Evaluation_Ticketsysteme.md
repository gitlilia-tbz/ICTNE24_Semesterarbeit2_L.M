1.2.1 Evaluation der Ticketsysteme

Diese Evaluation stützt sich auf die Grundlegenden Elemente der ITIL V4 ITSM Struktur.
![](3_ITSM_Grundlagen.png)

| 🤖 Disclamer: Diese Evaluation wurde durch Claude-AI gestützt          |
| ---------------------------------------------------------------------- |
| [Siehe diesen Link für weitere Informationen](./Quellen_und_Disclamer) |

| System    | ITSM-Funktion              | Kernfunktionen                              | Level         |
| --------- | -------------------------- | ------------------------------------------- | ------------- |
| ZAMMAD    | Incident Management        | Tickets, SLAs, Workflows, Multi-Channel     | Vollständig   |
|           | Change Management          | Change-Tickets, Genehmigungen, Risikofelder | Vollständig   |
|           | Problem Management         | Problem-Tickets, Incident-Linking, RCA      | Vollständig   |
|           | Knowledge Management       | KB, Kategorien, Suche, Versionen            | Vollständig   |
|           | IT Asset Management        | Asset-Tracking, Linking, Custom Fields      | Grundlegend   |
|           | Service Desk               | Multi-Channel, Portal, Routing, Tools       | Vollständig   |
|           | Service Catalog            | Request-Forms, Kategorien, Portal           | Grundlegend   |
|           | Service Request Management | Formulare, Workflows, Genehmigungen         | Grundlegend   |
| OTRS      | Incident Management        | ITIL-konform, SLAs, Multi-Channel           | Vollständig   |
|           | Change Management          | CAB, Workflows, Genehmigungen               | Vollständig   |
|           | Problem Management         | RCA, KEDB, Trendanalyse                     | Vollständig   |
|           | Knowledge Management       | CMDB-Integration, FAQ, Volltext             | Vollständig   |
|           | IT Asset Management        | CMDB, CI-Tracking, Lifecycle                | Vollständig   |
|           | Service Desk               | Multi-Channel, Portal, Reporting            | Vollständig   |
|           | Service Catalog            | Designer, SLA-Mgmt, Automatisierung         | Vollständig   |
|           | Service Request Management | Vollautomatisiert, Templates, Prozesse      | Vollständig   |
| FREESCOUT | Incident Management        | Basis-Ticketing, E-Mail, Prioritäten        | Grundlegend   |
|           | Change Management          | Manuelle Verfolgung, Kategorien             | Eingeschränkt |
|           | Problem Management         | Ticket-Linking, Dokumentation               | Eingeschränkt |
|           | Knowledge Management       | Basis-KB, Suche                             | Grundlegend   |
|           | IT Asset Management        | Keine native Funktion                       | Minimal       |
|           | Service Desk               | E-Mail-Support, Basis-Routing               | Grundlegend   |
|           | Service Catalog            | Keine native Funktion                       | Minimal       |
|           | Service Request Management | Basis E-Mail Anfragen                       | Minimal       |


Fazit:
- OTRS: Enterprise-Level, vollständige ITIL/ITSM-Funktionen.

:small_red_triangle: Nachteile:
Etwas komplexere Struktur, weniger Benutzerfreundlich

- ZAMMAD: Mittelweg, gute ITSM-Basics, moderne UI

:small_red_triangle: Nachteile: Im Vergleich zu OTRS weniger Vollständige Funktionsabdeckung

- FREESCOUT: Einfach, fokussiert auf E-Mail-Support

:small_red_triangle: Nachteile: Zu simpel, fehlende Funktionen. Nur 
grundlegender Email-Support


| Kriterien             | ZAMMAD | OTRS | FREESCOUT |
| --------------------- | ------ | ---- | --------- |
| Docker-Kompatibilität | ✓      | ±    | ±         |
| Agenten-Unterteilung  | ✓      | ✓    | ±         |
| Workflows             | ✓      | ✓    | ±         |
| API-Funktionalität    | ✓      | ✓    | -         |

Legende:
- ✓ Vollständig/Gut
- ± Grundlegend/Eingeschränkt
- - Minimal/Nicht vorhanden

	Anhand dieser Evaluation ist der Favorit: *Zammad Ticketing System*

		Um meine Evaluation in der Praxis zu stützen, habe ich mit Unterstützung von Claude AI Docker-Compose Files der verschiedenen Lösungen erstellt. Diese werden im $\color{yellow}{\textsf{ Arbeitspaket 3: Entscheiden}}$ getestet.

