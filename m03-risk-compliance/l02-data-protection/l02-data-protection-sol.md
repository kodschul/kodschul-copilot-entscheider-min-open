# Lab 3.2 – Lösung: Datenschutz und Compliance

Keine Rechtsberatung. Stand: 31.10.2026, vor Kursbeginn prüfen.

## Quiz

| # | Antwort | Begründung |
| -: | --- | --- |
| 1 | stimmt nicht | Der Vertrag bindet Microsoft; Zweck, Rechtsgrundlage, Verzeichnis, DSFA-Prüfung, Berechtigungen und Löschregeln bleiben beim Verantwortlichen. |
| 2 | stimmt nicht | Auch das Zusammenfassen einer Mail mit Namen und Inhalten über Personen ist eine Verarbeitung personenbezogener Daten. |
| 3 | stimmt nicht | Interaktionen und Memory enthalten personenbezogene Daten; Aufbewahrung und Löschung werden festgelegt und im Verzeichnis dokumentiert (Art. 5, 17, 30 DSGVO; Memory aus Lab 1.2). |
| 4 | stimmt nicht | Der EU AI Act gilt auch für Betreiber; die Pflicht zur KI-Kompetenz (Art. 4) trifft jede Organisation, die KI einsetzt. |

## Aufgabe 1: Einschätzung je Punkt

| # | Punkt | Einschätzung | Begründung |
| -: | --- | --- | --- |
| 1 | Auftragsverarbeitung | vorhanden, Abdeckung bestätigen | Nordwind nutzt Microsoft 365; der Auftragsverarbeitungsvertrag mit Microsoft ist Teil des Vertrags. Zu bestätigen ist, dass er Copilot umfasst. |
| 2 | Verzeichnis der Verarbeitungstätigkeiten | unklar | Kein Beleg, dass Copilot eingetragen ist. |
| 3 | Datenschutz-Folgenabschätzung | unklar | neue Technologie, Zugriff auf Mails und Besprechungen von 250 Beschäftigten, mögliche Rückschlüsse auf Verhalten: Prüfung nötig. |
| 4 | Aufbewahrung und Löschung | unklar | keine Regel für Interaktionen und Memory belegt. |
| 5 | KI-Kompetenz | fehlt | keine Schulung geplant; Pflicht seit 02.02.2025. |
| 6 | KI-Richtlinie | fehlt | keine Richtlinie, obwohl ein Drittel private KI-Werkzeuge nutzt (Lab 3.1). |

## Aufgabe 2: voreilige Einträge

| Eintrag in Abschnitt 7 | Befund |
| --- | --- |
| Datenschutz-Folgenabschätzung: **nicht nötig** | voreilig: Ob eine DSFA nötig ist, wird geprüft und dokumentiert, nicht vorab ausgeschlossen. |
| Aufbewahrung und Löschung: verantwortlich **IT** | unvollständig: Löschfristen sind eine Datenschutzfrage, IT setzt sie technisch um. |
| Auftragsverarbeitung: vorhanden | tragbar, aber ohne Prüfvermerk, ob Copilot abgedeckt ist. |

## Aufgabe 3 bis 5: Abschnitt 7 korrigiert

| Punkt | Status | Nächster Schritt | Verantwortlich |
| --- | --- | --- | --- |
| Auftragsverarbeitung mit Microsoft geprüft | vorhanden | Abdeckung von Copilot im Vertrag bestätigen | Datenschutz |
| Datenschutz-Folgenabschätzung | **unklar, prüfen** | vor dem Pilot prüfen, ob eine DSFA nötig ist, Ergebnis dokumentieren | Datenschutz |
| Aufbewahrung und Löschung von Copilot-Interaktionen | unklar | Fristen für Interaktionen und Memory festlegen, technisch umsetzen | **Datenschutz, IT** |
| KI-Kompetenz-Schulung (EU AI Act, Art. 4) | fehlt | rollenbasierte Schulung für die Pilotgruppe vor dem Pilotstart | HR |
| KI-Richtlinie | fehlt | Richtlinie in einfacher Sprache vor dem Pilot, mit verbotenen Nutzungen (Art. 9 DSGVO, Bewertung von Personen) | Geschäftsführung |
| Verzeichnis der Verarbeitungstätigkeiten ergänzt | unklar | Eintrag mit Zweck, Datenarten, Betroffenen, Fristen | Datenschutz |
| **Datenflüsse und MCP-Server für das CRM** | **unklar** | klären, wer den MCP-Server betreibt, wo er steht, ob ein eigener Vertrag nötig ist | IT, Datenschutz |
| **Agenten mit Personenbezug** | trifft für IT-Helfer nicht zu | vor jedem HR- oder Bewerbungs-Agenten gesondert prüfen (Hochrisiko nach EU AI Act möglich) | Datenschutz, HR |

Begründung der Zusatzpunkte: Abschnitt 4 plant das CRM zuerst anzubinden; damit entsteht ein neuer Datenweg. Der HR-Bereich arbeitet mit dem Bewerbungsprozess; ein Agent dort wäre ein Hochrisiko-Kandidat.

## Typische Lücken, die zusätzlich auffallen

| Lücke | Warum sie zählt |
| --- | --- |
| Information der Beschäftigten über die neue Verarbeitung | Transparenzpflicht der DSGVO (Art. 13); schafft zugleich Vertrauen |
| Regeln für Memory und Interaktionsverlauf | Memory speichert Fakten über Personen (Lab 1.2) |
| Teams-Transkription | Besprechungsinhalte aller Teilnehmenden werden verarbeitet; Regeln zu Ankündigung und Zustimmung |
| Mitarbeitervertretung nicht als Punkt aufgeführt | eigene Pflicht neben dem Datenschutz, vertieft in Lab 3.3 |

## Erweiterung

Häufig „unklar" in Organisationen: DSFA-Prüfung, Löschfristen für Interaktionen, Datenflüsse über neue Anbindungen. Geklärt werden sie meist von der Datenschutzbeauftragten mit IT und Rechtsabteilung.
