# Lab 2.1 – Übung: Eigene Agenten: Copilot für jede Aufgabe

**Ändert die Nordwind-Projektbasis?** Ja — Abschnitt 2 „Erste Agentenidee" in `nordwind-entscheidungsvorlage.md` wird geprüft und korrigiert; Lab 2.2 baut auf diesem Agenten auf.

## Quiz: Rückblick auf Modul 1

1. „Copilot sieht alle Dateien im Unternehmen." – stimmt / stimmt nicht
2. Was unterscheidet Microsoft 365 Copilot von Copilot Chat?
   - a) ein deutlich besseres Sprachmodell
   - b) Zugriff auf die eigenen Arbeitsdaten über Microsoft Graph und Copilot in den Apps
   - c) nur die Sprache der Oberfläche
3. Dieselbe Frage liefert bei zwei Personen unterschiedliche Antworten. Was ist der wichtigste Grund?
   - a) Zufall im Sprachmodell
   - b) unterschiedlicher Kontext: eigene Mails, Dateien, Berechtigungen, Memory
   - c) unterschiedliche Lizenzpreise

## Ausgangslage: Beispiel aus der Demo

Im Agent Builder entsteht der Agent „Nordwind IT-Helfer". Als Wissen dient `../../project/nordwind-it-richtlinie.md`.

**Anweisungen (Beispieltext):**

```text
Rolle: Du bist der IT-Helfer von Nordwind Consulting.
Aufgabe: Beantworte Standardfragen zu VPN, Geräten, Passwörtern und IT-Support-Kontakt.
Quellen: Antworte nur auf Basis der Nordwind-IT-Richtlinie und nenne den Abschnitt.
Stil: höchstens fünf Sätze, sachlich, mit dem nächsten Schritt.
Grenzen: Sonderberechtigungen, Gehalt und persönliche Ausnahmen beantwortest du nicht.
Verweise dann an das IT-Ticket-Portal bzw. an HR. Erfinde keine Angaben.
```

**Zwei Testfragen:**

| Testfrage | Erwartetes Verhalten | Beispielantwort des Agenten |
| --- | --- | --- |
| „Welches VPN nutzen wir und wie melde ich mich an?" | beantwortet aus der Richtlinie, nennt die Quelle | „Nordwind nutzt den Cisco Secure Client (AnyConnect), vorinstalliert auf allen Firmengeräten. Verbindungsziel eingeben, dann mit Firmen-Login und Authenticator-App anmelden (IT-Richtlinie, Abschnitt VPN und Remote-Zugriff)." |
| „Kann ich für mein Projekt Admin-Rechte auf meinem Laptop bekommen?" | außerhalb der Richtlinie: keine eigene Regel erfinden, an IT-Support verweisen | „Sonderberechtigungen regelt die IT-Richtlinie nicht. Bitte ein Ticket im IT-Ticket-Portal anlegen (Abschnitt Eskalation)." |

Drei mögliche erste Agenten für Nordwind (aus der Theorie):

- IT-Helfer (IT-Richtlinie),
- Onboarding-Begleiter (Onboarding-Leitfaden),
- Angebotsassistent (Angebotsvorlage, Formulierungsregeln).

## Aufgaben

1. Beantworte die drei Quizfragen, bevor die Lösung geöffnet wird.
2. Lies die Beispielanweisungen und markiere je eine Zeile für Rolle, Quelle und Grenze.
3. Wähle aus den drei Agenten den ersten für Nordwind und begründe die Wahl in einem Satz.
4. Öffne `../../project/nordwind-entscheidungsvorlage.md`, Abschnitt 2 „Erste Agentenidee". Prüfe Name, Zweck, Wissen und Nutzergruppe: Was stimmt, was ist zu weit gefasst?
5. Korrigiere die Felder, die nicht passen, direkt in der Tabelle und notiere den Grund in einem Satz unter der Tabelle.

## Checkpoint

- Drei Quizantworten sind notiert.
- Rolle, Quelle und Grenze sind in den Anweisungen markiert.
- Abschnitt 2 der Entscheidungsvorlage enthält mindestens eine Korrektur mit Begründung.

## Abschlusskriterien

- Abschnitt 2 nennt Zweck, Wissen und eine Nutzergruppe, die zum Wissen passt.
- Die Wahl des ersten Agenten ist in einem Satz begründet.

## Erweiterung

- Prüfe die zweite Testfrage: Woran ist erkennbar, dass der Agent nichts erfunden hat? Notiere einen Satz.
- Formuliere eine dritte Testfrage, die der Agent an HR verweisen muss, und notiere das erwartete Verhalten.
- Schreibe für den Onboarding-Begleiter einen eigenen Anweisungstext nach dem Muster oben (Rolle, Aufgabe, Quellen, Stil, Grenzen) auf Basis von `../../project/nordwind-onboarding-leitfaden.md`.
