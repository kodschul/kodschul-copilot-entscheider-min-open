# Lab 2.3 – Lösung: KI mit allem verbinden: MCP

## Aufgabe 1: Eigene Antworten

Keine feste Lösung. Gut begründbar: (1) CRM, weil Vertrieb und Projektleitungen es vor jedem Kundentermin brauchen; (2) nur lesen; (3) vorerst nicht anbinden.

## Aufgabe 2: Entwurf gegen die Daten geprüft

| Angabe im Entwurf | Daten | Richtig |
| --- | --- | --- |
| CRM: „lesen und schreiben" | nur lesen 70 %, lesen und schreiben 30 % | **nur lesen** |
| ERP: „Zuerst? ja" | ERP zuerst: 10 % | **nein** |
| ERP: „lokales Modell (Mehrheit)" | lokal 45 %, vorerst nicht 35 %, Cloud 20 % | **keine Mehrheit**; größte Gruppe „lokal", aber 55 % wählen eine andere Option |
| „klar für eine schnelle Anbindung von CRM und ERP" | CRM 55 %, ERP 10 % | **nur CRM**; ERP klar nicht zuerst |

## Aufgabe 3: Annahmen des KI-Werkzeugs

- Modell für CRM und Ticketsystem („Cloud-Modell") wurde nicht abgefragt.
- Zugriff „lesen" für das Ticketsystem wurde nicht abgefragt.
- ERP-Zugriff „lesen" wurde nicht abgefragt.

Das KI-Werkzeug hat Lücken plausibel aufgefüllt, ohne das zu kennzeichnen; genau deshalb wird jede Zusammenfassung gegen die Rohdaten geprüft.

## Aufgabe 4 und 5: Abschnitt 4 korrigiert

| System | Zuerst? | Zugriff | Modell |
| --- | --- | --- | --- |
| CRM | ja | **zuerst nur lesen**; schreiben frühestens nach dem Lesebetrieb und mit Bestätigung durch einen Menschen | **Cloud-Modell (Microsoft 365 Copilot)**, Kundendaten bleiben im bestehenden Microsoft-365-Rahmen |
| Ticketsystem IT | später | lesen | **Cloud-Modell**, keine besonders sensiblen Daten |
| ERP / Buchhaltung | nein | – | **vorerst keines**; Budgets, Zeiterfassung und Personaldaten später mit lokalem Modell prüfen |

**Begründung:** „Lesen und schreiben" von Beginn an verbindet die größte Fehlerfolge (falsche Einträge im CRM) mit der geringsten Erfahrung. Die Modellspalte macht sichtbar, dass sensible Systeme eine eigene Entscheidung brauchen.

## Aufgabe 6: Betreiber-Prüffrage für das CRM

- „Bietet der CRM-Hersteller einen eigenen MCP-Server an, wo läuft er, und lässt sich der Zugriff auf Lesefunktionen begrenzen?"

Gleichwertig: „Wer in der IT ist Owner des MCP-Servers und mit welchen CRM-Rechten läuft er?"
