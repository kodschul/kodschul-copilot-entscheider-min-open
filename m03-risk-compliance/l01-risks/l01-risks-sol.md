# Lab 3.1 – Lösung: Risiken erkennen und begrenzen

## Quiz

| # | Antwort | Begründung |
| -: | --- | --- |
| 1 | b | Ein Skill ist eine Markdown-Datei (`SKILL.md`) mit einer Anleitung, die ein Agent nur bei Bedarf lädt (Lab 2.2). |
| 2 | a | Jedes System stellt seine Funktionen einmal als MCP-Server bereit; jeder kompatible Assistent nutzt sie. Fünfzehn Einzelverbindungen wären es ohne Standard (Lab 2.3). |
| 3 | b | Risiko 3 heißt: erst nach den Maßnahmen aus Modul 3 starten, nicht ablehnen (`bewertungsmatrix.md`). |

## Aufgabe 1: vorhandene Einträge prüfen

| Eintrag | Befund |
| --- | --- |
| fehlerhafte Inhalte in Kundentexten · mittel · hoch · Prüfpflicht vor Versand · Projektleitungen | plausibel und konkret; bleibt. |
| Kosten ohne Nutzung · mittel · mittel · Lizenzen nach Nutzung vergeben · IT | plausibel; Gegenmaßnahme schärfen: Nutzung nach 60 Tagen auswerten, ungenutzte Lizenzen umverteilen. |

Größter Befund: Die beiden Risiken, die bei Nordwind schon heute nachweisbar sind (Oversharing, Schatten-KI), fehlen ganz.

## Aufgabe 2: Abschnitt 6 für den Top-Fall ergänzt

Top-Fall aus Lab 2.4: **Fall D – IT-Helfer**, Stufe 2, Nutzen 3 / Machbarkeit 3 / Risiko 1, Priorität 6.

| Risiko | Wahrscheinlichkeit | Auswirkung | Gegenmaßnahme | Verantwortlich |
| --- | --- | --- | --- | --- |
| fehlerhafte Inhalte in Kundentexten | mittel | hoch | Prüfpflicht vor Versand | Projektleitungen |
| Kosten ohne Nutzung | mittel | mittel | Lizenzen nach Nutzung vergeben, Nutzung nach 60 Tagen auswerten | IT |
| **Oversharing:** Ordner mit Freigabe „alle Mitarbeitenden", auch Angebotskalkulationen | hoch | hoch | Freigaben vor dem Pilot prüfen und einschränken, sensible Dateien kennzeichnen | IT mit Bereichsleitungen |
| **Schatten-KI:** ein Drittel nutzt private KI-Werkzeuge, teils mit Kundendaten | hoch | hoch | Copilot Chat als freigegebenes Werkzeug, KI-Richtlinie mit verbotenen Nutzungen und Meldeweg | Geschäftsführung |
| **Fehlerhafte Inhalte im Top-Fall:** IT-Helfer antwortet mit veralteter Richtlinie | mittel | mittel | Owner und Prüfturnus für Agent und `nordwind-it-richtlinie.md`, Hinweis auf Ticket-Portal | IT |
| **Teilen über die Nutzergruppe hinaus:** IT-Helfer wird mit externen Partnern geteilt | mittel | hoch | Nutzergruppe nur interne Mitarbeitende (Lab 2.1), Freigabe vor jedem Teilen | IT |
| **Abhängigkeit:** Erfahrungswissen bei wenigen Personen, IT-Helfer wird nicht gepflegt | mittel | mittel | Wissen als Skill festhalten (Lab 2.2), Owner benennen | IT |

Begründung: Oversharing und Schatten-KI sind bei Nordwind belegt (Ausgangslage) und haben hohe Wahrscheinlichkeit und hohe Auswirkung; ohne sie ist der Abschnitt nicht entscheidungsfähig. Die übrigen neuen Einträge betreffen den IT-Helfer direkt.

## Aufgabe 3: KI-Zusammenfassung prüfen

| Aussage der KI | Bewertung | Beleg |
| --- | --- | --- |
| Oversharing in allen drei Matrizen | **falsch** | nur Matrix 1 und 3 |
| fehlerhafte Inhalte in allen drei Matrizen | belegt | M1 veraltete Anleitung, M2 falsche Antwort, M3 erfundene Zahlen |
| Schatten-KI in zwei Matrizen | **falsch** | nur Matrix 2 |
| Matrix 3: zwei Risiken ohne Maßnahme und Rolle | belegt | Kalkulationen, Nachrechnen |
| Kosten ohne Nutzung kommt nicht vor | **falsch** | Matrix 1 „Lizenzen bleiben ungenutzt", aber ohne Rolle |
| Verantwortlich für Oversharing: Datenschutz | **nicht belegt** | in den Matrizen steht IT bzw. keine Rolle |
| — | **fehlt** | Matrix 1: Kostenrisiko ohne Rolle; Teilen mit Externen (M2) wird nicht erwähnt |

Korrigierte Zusammenfassung:

```text
Die drei häufigsten Risiken:
1. Fehlerhafte Inhalte – in allen drei Matrizen.
2. Oversharing (Kalkulationen für alle freigegeben) – in zwei Matrizen, in Matrix 3 ohne Maßnahme.
3. Je einmal: Schatten-KI, Teilen mit Externen, Kosten ohne Nutzung, Abhängigkeit.

Lücken:
- Matrix 3: zwei Risiken ohne Maßnahme und ohne Rolle.
- Matrix 1: Kosten ohne Nutzung ohne Rolle.
- Schatten-KI fehlt in zwei Matrizen, obwohl es bei Nordwind belegt ist.

Empfehlung: Oversharing vor dem Pilot beheben, verantwortlich: IT mit den Bereichsleitungen.
```

Lehre: Auch eine Zusammenfassung über MCP wird gegen die gelesenen Daten geprüft; Zählungen und Rollen sind die typischen Fehlerstellen.

## Erweiterung

### Auffälligkeiten zuordnen

| Auffälligkeit in der Ausgangslage | Risikoklasse |
| --- | --- |
| viele Projektordner für „alle Mitarbeitenden" freigegeben, auch Angebotskalkulationen | 2 – Oversharing |
| ein Drittel nutzt private KI-Werkzeuge, teils mit Kundendaten | 3 – Schatten-KI |
| Erfahrungswissen steckt bei wenigen langjährigen Personen | 4 – Abhängigkeit und Kompetenzverlust (verschärft sich, wenn Wissen nur im Agenten steckt und niemand es pflegt) |
| 60 % der IT-Tickets zu denselben zehn Themen | kein Risiko, sondern der Nutzen des Top-Falls; Risiko 1 entsteht, wenn der Agent veraltete Antworten gibt |
| Wiki teilweise veraltet (Systemlandschaft) | 1 – fehlerhafte Inhalte, sobald das Wiki als Kontext dient |

### Matrix für den Top-Fall

Top-Fall aus Lab 2.4: **Fall D – IT-Helfer**, Stufe 2, Nutzen 3 / Machbarkeit 3 / Risiko 1, Priorität 6.

| Risiko | W | A | Gegenmaßnahme | Rolle |
| --- | --- | --- | --- | --- |
| Agent antwortet mit veralteter Richtlinie (z. B. VPN, Passwortregeln) | mittel | mittel | Owner für `nordwind-it-richtlinie.md`, Prüfturnus halbjährlich und bei Änderung; Hinweis auf Ticket-Portal in jeder Antwort | IT |
| Oversharing: Copilot-Lizenzen im Pilot machen freigegebene Kalkulationen auffindbar | hoch | hoch | Freigaben „alle Mitarbeitenden" vor dem Pilot prüfen und einschränken, Kalkulationen als „vertraulich" kennzeichnen | IT mit Bereichsleitungen |
| Agent wird über die Nutzergruppe hinaus geteilt (z. B. an externe Partner) | mittel | hoch | Nutzergruppe nur interne Mitarbeitende (Lab 2.1), Freigabe vor jedem Teilen | IT |
| Schatten-KI bleibt, weil Nutzende nur den IT-Helfer, aber kein allgemeines Werkzeug haben | hoch | hoch | Copilot Chat als freigegebenes Werkzeug für alle, KI-Richtlinie mit Meldeweg | Geschäftsführung, IT |
| Agent beantwortet Fragen außerhalb der Richtlinie (Sonderberechtigungen, Personalfragen) | niedrig | mittel | Eskalationsregel aus der Richtlinie in die Anweisungen übernehmen, zwei Testfragen vor Freigabe | IT |

Einordnung in die Matrix:

| W ↓ / A → | niedrig | mittel | hoch |
| --- | --- | --- | --- |
| **hoch** | | | Oversharing, Schatten-KI |
| **mittel** | | veraltete Richtlinie | Teilen über Nutzergruppe hinaus |
| **niedrig** | | Fragen außerhalb der Richtlinie | |

Folge: Oversharing und Schatten-KI werden vor dem Pilot behandelt; obwohl der Fall selbst ein niedriges Risiko hat, betreffen beide jede Copilot-Lizenz.

### Oversharing in der eigenen Organisation

Typische Orte mit Oversharing: alte Projekt- und Angebotsordner, HR-Ablagen mit Vorlagen und Einzelfällen, Finanz-Exporte in Team-Sites, Ordner mit Freigabelinks für „alle mit dem Link". Prüfende Rolle: jeweils die fachlich verantwortliche Bereichsleitung zusammen mit der IT.

## Fallback

Mit Export-Datei statt MCP liefert das KI-Werkzeug eine gleichartige Zusammenfassung; die Prüfung und das Ergebnis oben gelten unverändert.
