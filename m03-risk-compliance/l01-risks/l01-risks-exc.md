# Lab 3.1 – Übung: Risiken erkennen und begrenzen

**Ändert die Nordwind-Projektbasis?** Ja — Abschnitt 6 „Risiken" der Entscheidungsvorlage wird geprüft und ergänzt.

## Ausgangslage

Bereitgestellt in `output/project/`:

- `nordwind-entscheidungsvorlage.md` — Abschnitt 5 (Top-Anwendungsfall aus Lab 2.4) und Abschnitt 6 (Risiken, vorbefüllt mit zwei Einträgen),
- `nordwind-ausgangslage.md` — Abschnitt „Auffälligkeiten" mit den bekannten Schwachstellen bei Nordwind.

Ist Abschnitt 5 noch leer, gilt als Top-Fall **Fall D – IT-Helfer** aus der [Lösung von Lab 2.4](../../m02-agents-integration/l04-prioritization/l04-prioritization-sol.md).

## Quiz

Kurzquiz zu Modul 2. Antwort je Frage notieren.

1. Was ist ein Skill?
   a) eine Zusatzlizenz für Copilot
   b) eine Markdown-Datei mit einer Anleitung für eine abgegrenzte Aufgabe, die ein Agent bei Bedarf lädt
   c) ein Programm, das ein Fachsystem an Microsoft 365 anschließt
2. Fünf Systeme, drei kompatible Assistenten. Wie viele MCP-Server braucht es, damit jeder Assistent jedes System nutzen kann?
   a) fünf
   b) acht
   c) fünfzehn
3. „Ein Fall mit Risiko 3 in der Bewertungsmatrix wird abgelehnt." Stimmt das?
   a) stimmt
   b) stimmt nicht

## Aufgaben

1. Prüfe die zwei vorhandenen Einträge in Abschnitt 6: Ist die Einschätzung plausibel, ist die Gegenmaßnahme konkret, ist eine Rolle benannt?
2. Ergänze Abschnitt 6 für den Top-Fall aus Abschnitt 5 auf mindestens vier Risiken. Nutze dafür die „Auffälligkeiten" in `nordwind-ausgangslage.md`: Jede dort belegte Risikoklasse aus der Theorie bekommt einen Eintrag mit Wahrscheinlichkeit, Auswirkung, Gegenmaßnahme und verantwortlicher Rolle.
3. Prüfe die KI-Zusammenfassung aus dem Beispiel unten gegen die drei Matrizen. Markiere jede Aussage als „belegt", „falsch" oder „fehlt" und notiere die korrigierte Zusammenfassung.

### Beispiel aus der Demo: Matrizen per MCP zusammenfassen

Ein KI-Werkzeug liest über eine MCP-Anbindung an das Whiteboard-Werkzeug (Prinzip wie in Lab 2.3) drei Risikomatrizen und fasst sie zusammen. Gelesene Daten (gekürzt):

```text
Matrix 1 – Top-Fall: IT-Helfer
  - Agent nennt veraltete VPN-Anleitung        | W: mittel | A: mittel | Maßnahme: Prüfturnus Richtlinie       | Rolle: IT
  - Kalkulationen für alle freigegeben         | W: hoch   | A: hoch   | Maßnahme: Freigaben prüfen            | Rolle: IT
  - Lizenzen bleiben ungenutzt                 | W: mittel | A: mittel | Maßnahme: Nutzung nach 60 Tagen prüfen | Rolle: –

Matrix 2 – Top-Fall: IT-Helfer
  - private KI-Werkzeuge mit Kundendaten       | W: hoch   | A: hoch   | Maßnahme: KI-Richtlinie               | Rolle: Geschäftsführung
  - Agent wird mit externen Partnern geteilt   | W: mittel | A: hoch   | Maßnahme: nur interne Nutzergruppe    | Rolle: IT
  - falsche Antwort zu Passwortregeln          | W: mittel | A: niedrig| Maßnahme: Hinweis „Antwort prüfen"    | Rolle: IT

Matrix 3 – Top-Fall: Angebotsassistent
  - erfundene Zahlen im Angebot                | W: mittel | A: hoch   | Maßnahme: Prüfpflicht vor Versand     | Rolle: Vertrieb
  - Kalkulationen für alle freigegeben         | W: hoch   | A: hoch   | Maßnahme: –                           | Rolle: –
  - niemand rechnet Angebote mehr selbst nach  | W: niedrig| A: mittel | Maßnahme: –                           | Rolle: –
```

W = Wahrscheinlichkeit, A = Auswirkung. Zusammenfassung des KI-Werkzeugs:

```text
Die drei häufigsten Risiken:
1. Oversharing (Kalkulationen für alle freigegeben) – in allen drei Matrizen.
2. Fehlerhafte Inhalte (veraltete, falsche oder erfundene Antworten) – in allen drei Matrizen.
3. Schatten-KI (private KI-Werkzeuge) – in zwei Matrizen.

Lücken:
- Matrix 3: zwei Risiken ohne Maßnahme und ohne Rolle.
- Kosten ohne Nutzung kommt in keiner Matrix vor.

Empfehlung: Oversharing vor dem Pilot beheben, verantwortlich: Datenschutz.
```

## Checkpoint

- Abschnitt 6 enthält für den Top-Fall mindestens vier Risiken, jedes mit Gegenmaßnahme und Rolle.
- Jede Aussage der KI-Zusammenfassung ist als „belegt", „falsch" oder „fehlt" markiert.

## Abschlusskriterien

- Abschnitt 6 in `nordwind-entscheidungsvorlage.md` enthält die bisher fehlenden Risikoklassen, jeweils mit Wahrscheinlichkeit, Auswirkung, Gegenmaßnahme und Verantwortlich.
- Kein Eintrag in Abschnitt 6 hat eine leere Rolle.

## Erweiterung

- Ordne jede Auffälligkeit aus `nordwind-ausgangslage.md` einer der fünf Risikoklassen zu und trage die Risiken in eine Matrix Wahrscheinlichkeit × Auswirkung ein.
- Die eigene Organisation als Beispiel nehmen: drei Orte benennen, an denen vermutlich Oversharing besteht, und je eine Rolle, die die Freigaben prüfen könnte. Im Plenum oder allein, ohne vertrauliche Details.

## Fallback

Ohne MCP-Anbindung an das Whiteboard: die Matrizen als Export-Datei an das KI-Werkzeug geben oder die Zusammenfassung oben verwenden. Einschränkung: Die Daten sind dann nicht live, die Prüfaufgabe bleibt gleich.
