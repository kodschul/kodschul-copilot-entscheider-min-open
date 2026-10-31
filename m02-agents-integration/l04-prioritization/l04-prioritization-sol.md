# Lab 2.4 – Lösung: Anwendungsfälle bewerten und priorisieren

## Aufgabe 1 und 2: Quiz „Welche Stufe?"

| Quizfall | Fall in der Galerie | Stufe | Begründung |
| --- | --- | --- | --- |
| 1 Monatsbericht Controlling | C | **1 – Apps** | Die Tabellen liegen in SharePoint; Copilot in Excel reicht, kein eigener Agent nötig. |
| 2 Angebote nach Hausregeln | F | **2 – Agent** | Die Regeln müssen als Wissensdatei bzw. Skill festgehalten und in einem Agenten hinterlegt werden. |
| 3 Kundenstatus aus dem CRM | G | **3 – Anbindung** | Das CRM liegt außerhalb von Microsoft 365 und muss angebunden werden (lesend). |

Häufige Fehleinschätzung: Fall 1 als Agent. Ein Agent lohnt erst, wenn feste Regeln oder Wissen dazukommen, die jedes Mal wieder erklärt werden müssten.

## Aufgabe 3 und 4: Bewertung und Priorität

| Fall | Stufe | Nutzen | Machbarkeit | Risiko | Priorität | Gründe |
| --- | --- | ---: | ---: | ---: | ---: | --- |
| D IT-Helfer | 2 | 3 | 3 | 1 | **6** | alle Mitarbeitende, täglich, 60 % der Tickets; Richtlinie liegt vor, Agent in Minuten angelegt; intern, keine Personendaten |
| E Onboarding-Begleiter | 2 | 2 | 2 | 1 | 4 | ca. 40 Personen pro Jahr, entlastet HR wöchentlich; Skill muss erst erstellt und geprüft werden; Personalfragen sind per Grenze ausgeschlossen |
| G Kundenstatus CRM | 3 | 2 | 1 | 2 | 3 | Vertrieb und Projektleitungen, wöchentlich; Fachsystem muss angebunden werden; Kundendaten |

**Top-Fall: D IT-Helfer.** Höchste Priorität bei geringstem Risiko; der Vorher-Wert (60 % Standardtickets) liegt bereits vor.

Hinweis: Fall A (Mailverläufe) erreicht ebenfalls Priorität 6. Er läuft aber in Stufe 1 ohne eigene Einrichtung mit, sobald Lizenzen vergeben sind; als erster eigener Anwendungsfall eignet sich D, weil sein Erfolg über das Ticketsystem messbar ist.

## Aufgabe 5: Erfolgskriterium

„IT-Tickets zu den zehn Standardthemen (VPN, Passwort, Geräte) sinken innerhalb von 90 Tagen nach dem Start des IT-Helfers von 60 % auf 40 % aller IT-Tickets."

Vorher-Wert: 60 % (Ausgangslage) · Zielwert: 40 % · Frist: 90 Tage.

## Aufgabe 6: Abschnitt 5 ausgefüllt

| Feld | Entwurf | Korrektur |
| --- | --- | --- |
| Fall | – | **Fall D – IT-Helfer** |
| Stufe | – | **2 – Agent** |
| Bewertung (Nutzen / Machbarkeit / Risiko) | – | **3 / 3 / 1 → Priorität 6** |
| Erfolgskriterium | Mitarbeitende sind zufriedener | **Tickets zu den zehn Standardthemen sinken in 90 Tagen von 60 % auf 40 %.** |

**Begründung:** „Zufriedener" hat weder Vorher-Wert noch Zielwert noch Frist und lässt sich nach dem Pilot nicht prüfen.

## Erweiterung: Fall H

| Fall | Stufe | Nutzen | Machbarkeit | Risiko | Priorität |
| --- | --- | ---: | ---: | ---: | ---: |
| H Tickets aus Mails anlegen | 3 | 2 | 1 | 3 | 3 |

Risiko 3 wegen schreibendem Zugriff. Maßnahme vor dem Start: Der Agent legt nur einen Ticket-Entwurf an, ein Mensch bestätigt vor dem Speichern; vorher einige Wochen nur lesend testen (Lab 2.3).
