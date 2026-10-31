# Lab 2.1 – Lösung: Eigene Agenten: Copilot für jede Aufgabe

## Aufgabe 1: Quiz

| Frage | Antwort | Begründung |
| --- | --- | --- |
| 1 | stimmt nicht | Copilot arbeitet nur im Rahmen der Berechtigungen der jeweiligen Person (Lab 1.1). |
| 2 | b | Den Unterschied macht der Zugriff auf Arbeitsdaten über Microsoft Graph und Copilot in den Apps, nicht ein anderes Modell (Lab 1.1). |
| 3 | b | Antwortqualität = Modell × Kontext; Postfach, Dateien, Berechtigungen und Memory sind je Person verschieden (Lab 1.2). |

## Aufgabe 2: Bausteine in den Anweisungen

| Baustein | Zeile |
| --- | --- |
| Rolle | „Du bist der IT-Helfer von Nordwind Consulting." |
| Quelle | „Antworte nur auf Basis der Nordwind-IT-Richtlinie und nenne den Abschnitt." |
| Grenze | „Sonderberechtigungen, Gehalt und persönliche Ausnahmen beantwortest du nicht." |

## Aufgabe 3: Erster Agent

**IT-Helfer.** Das Wissen liegt bereits als Richtlinie vor, rund 60 % der IT-Tickets betreffen dieselben zehn Themen, und es sind keine Personendaten im Spiel.

Vertretbare Alternative: Onboarding-Begleiter, wenn HR stärker entlastet werden soll; das Vorgehen kennen dort aber nur zwei Personen und es ist noch nicht vollständig aufgeschrieben (Thema von Lab 2.2).

## Aufgabe 4 und 5: Abschnitt 2 korrigiert

| Feld | Entwurf | Korrektur |
| --- | --- | --- |
| Name | Nordwind IT-Helfer | unverändert |
| Zweck | Standardfragen zu VPN, Geräten und Passwörtern beantworten | unverändert; ergänzt: „Sonderfälle an das IT-Ticket-Portal verweisen" |
| Wissen | IT-Richtlinie, Onboarding-Leitfaden | unverändert |
| Nutzergruppe | alle Mitarbeitenden und externe Partner | **interne Mitarbeitende von Nordwind; externe Partner ausgenommen** |

**Begründung:** Richtlinie und Leitfaden sind interne Dokumente (VPN-Ziel, Support-Wege, Abläufe). Ein mit Externen geteilter Agent würde diese Inhalte nach außen geben; das ist eine zu weit gefasste Freigabe (Oversharing, vertieft in Lab 3.1). Start mit internen Mitarbeitenden, Ausweitung nur nach eigener Prüfung.

## Erweiterung: Nichts erfunden

Der Agent nennt keine eigene Regel zu Admin-Rechten, sagt ausdrücklich, dass die Richtlinie das nicht regelt, und verweist auf den Weg aus dem Abschnitt „Eskalation".

## Erweiterung: Dritte Testfrage

| Testfrage | Erwartetes Verhalten |
| --- | --- |
| „Wie viele Urlaubstage habe ich in der Probezeit?" | keine Zahl nennen; sagen, dass die IT-Richtlinie das nicht abdeckt, und an HR verweisen |

Gleichwertig: Fragen zu Gehalt, Vertrag oder persönlichen Ausnahmen.

## Erweiterung: Anweisungen für den Onboarding-Begleiter

```text
Rolle: Du bist der Onboarding-Begleiter von Nordwind Consulting.
Aufgabe: Beantworte Fragen neuer Mitarbeitender zu den ersten 30 Tagen:
erster Arbeitstag, Geräte und Zugänge, Ansprechpersonen, Pflichtschulungen.
Quellen: Antworte nur auf Basis des Onboarding-Leitfadens und nenne den Abschnitt.
Stil: freundlich, höchstens fünf Sätze, mit dem nächsten Schritt.
Grenzen: Gehalt, Vertrag, Probezeitbewertung und persönliche Ausnahmen beantwortest du nicht;
verweise dann an HR. Keine Angaben über andere Personen.
```
