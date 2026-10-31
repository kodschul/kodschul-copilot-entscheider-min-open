# Lab 2.2 – Übung: KI baut KI: Skills und Markdown-Dateien

**Ändert die Nordwind-Projektbasis?** Ja — Abschnitt 3 „Wissen als Skill" in `nordwind-entscheidungsvorlage.md` wird ergänzt.

## Ausgangslage: Beispiel aus der Demo

Die Assistenten-Kette aus dem [Anhang](../anhang-assistenten-prompts.md) lief in Copilot Chat mit dieser Problembeschreibung:

```text
Neue Mitarbeitende fragen in den ersten 30 Tagen immer dasselbe: Laptop, Zugänge,
Ansprechpersonen, Schulungen. Das Vorgehen kennen nur zwei Personen in HR.
Grundlage: Onboarding-Leitfaden und IT-Richtlinie.
```

**Zwischenergebnis 1 – Problem-Solver (gekürzt):**

| Feld | Ergebnis |
| --- | --- |
| Problem | wiederkehrende Standardfragen; Vorgehen hängt an zwei Personen |
| Zielgruppe | ca. 40 neue Mitarbeitende pro Jahr, entlastet werden HR und IT |
| Datenquellen | Onboarding-Leitfaden, IT-Richtlinie (vorhanden) |
| Risiken | veralteter Leitfaden; Fragen zu Gehalt oder Vertrag |
| Top-Empfehlung | Onboarding-Fragen mit festem Vorgehen beantworten, Sonderfälle an HR |

**Zwischenergebnis 2 – Solution Architect (gekürzt):**

- Erste Version: kein neuer Agent, sondern ein Skill `nordwind-onboarding-fragen` für den bestehenden Nordwind-Agenten aus Lab 2.1.
- Wissen: Onboarding-Leitfaden und IT-Richtlinie.
- Grenzen: Gehalt, Vertrag, Probezeitbewertung, persönliche Ausnahmen → HR.
- Später möglich: zweiter Skill „Checkliste für die erste Woche erstellen".

**Zwischenergebnis 3 – Skill-Generator:** ein `SKILL.md`-Entwurf. Bei der Prüfung gegen den Leitfaden fiel eine Abweichung auf:

| Entwurf | Leitfaden | Korrektur |
| --- | --- | --- |
| „Die Zugangsdaten kommen per E-Mail." | Zugangsdaten gehen per SMS an die private Nummer, nicht per E-Mail. | auf SMS korrigiert |

Die geprüfte Fassung liegt in `../../project/skills/nordwind-onboarding-fragen/SKILL.md`. Sie wurde dem Nordwind-Agenten zusammen mit `../../project/nordwind-onboarding-leitfaden.md` als Wissensdatei mitgegeben.

**Vorher / nachher:**

| Frage | Vorher (nur IT-Richtlinie) | Nachher (mit Leitfaden und Skill-Datei) |
| --- | --- | --- |
| „Wann bekomme ich Zugriff auf die Projektunterlagen?" | „Dazu enthält die IT-Richtlinie keine Angabe. Bitte an den IT-Support wenden." | „Der Zugriff auf Projektablagen wird schrittweise von der jeweiligen Projektleitung freigegeben, nicht automatisch am ersten Tag (Onboarding-Leitfaden, Erste 30 Tage). Nächster Schritt: bei der Projektleitung nachfragen." |
| „Wie ist die Gehaltsbandbreite in meiner Probezeit?" | „Dazu enthält die IT-Richtlinie keine Angabe." | „Dazu gibt dieser Assistent keine Auskunft. Bitte direkt an HR wenden." |

## Aufgaben

1. Lies die drei Zwischenergebnisse und notiere je Schritt die Entscheidung, die ein Mensch treffen musste.
2. Öffne `../../project/skills/nordwind-onboarding-fragen/SKILL.md` und markiere `name`, `description`, Vorgehen und Grenzen.
3. Prüfe zwei Angaben aus dem Beispiel am Ende der `SKILL.md` gegen `../../project/nordwind-onboarding-leitfaden.md` und `../../project/nordwind-it-richtlinie.md`. Notiere je Angabe „belegt" oder „nicht belegt" mit Fundstelle.
4. Entscheide für die `SKILL.md`: Wissensdatei oder Skill? Begründe in einem Satz, was sich für die Antwort ändert.
5. Öffne `../../project/nordwind-entscheidungsvorlage.md`, Abschnitt 3 „Wissen als Skill". Prüfe Erfahrungswissen und Format, trage Owner und Prüfturnus ein.
6. Nenne ein zweites Erfahrungswissen aus `../../project/nordwind-ausgangslage.md`, das als nächstes als Skill festgehalten werden sollte, und notiere es unter der Tabelle (im Plenum oder allein).

## Checkpoint

- Je Schritt der Kette ist eine menschliche Entscheidung notiert.
- Zwei Angaben aus der `SKILL.md` sind mit Fundstelle geprüft.
- Abschnitt 3 hat keine leeren Felder mehr.

## Abschlusskriterien

- Owner ist eine Rolle mit fachlicher Verantwortung, der Prüfturnus enthält einen festen Zeitraum und einen Anlass.
- Ein zweiter Skill-Kandidat ist benannt.

## Erweiterung

Lass die drei Assistenten aus dem Anhang in Copilot Chat für das zweite Erfahrungswissen laufen und prüfe den erzeugten `SKILL.md`-Entwurf gegen die Quellen. Voraussetzung: Zugang zu Copilot Chat; keine vertraulichen Daten in die Problembeschreibung schreiben.
