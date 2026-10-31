# Lab 3.2: Datenschutz und Compliance

**Leitfragen:**

<details>
<summary>Welche Daten im eigenen Bereich dürfen das Haus nie verlassen?</summary>

Typisch: Gesundheits- und Personaldaten, Geschäftsgeheimnisse, Daten mit vertraglicher Geheimhaltung. Für sie wird entschieden, ob ein Cloud-Dienst mit Vertrag reicht oder nur ein lokales Modell (Lab 2.3) infrage kommt.

</details>

<details>
<summary>Ist es ein Unterschied, ob ein Name eingetippt oder in einer vorhandenen Mail zusammengefasst wird?</summary>

Rechtlich nein: In beiden Fällen verarbeitet Copilot personenbezogene Daten. Praktisch ja: Beim Zusammenfassen fließen oft viel mehr Personendaten ein, als der Person bewusst ist.

</details>

<details>
<summary>Wer muss im eigenen Haus zustimmen, bevor ein neues Werkzeug mit Personendaten arbeitet?</summary>

Entscheiden muss die Leitung als Verantwortliche; beraten und prüfen die Datenschutzbeauftragte, die IT-Sicherheit und meist die Mitarbeitervertretung (Lab 3.3). Wer genau zustimmt, regelt das eigene Haus.

</details>

- Mit Copilot ändert sich nicht, welches Recht gilt, sondern wie viele Daten in einer Anfrage zusammenkommen.
- Der Vertrag mit Microsoft deckt den Dienst ab; Zweck, Berechtigungen, Dokumentation und Schulung bleiben Aufgabe der eigenen Organisation.
- Der EU AI Act verlangt schon heute KI-Kompetenz von allen, die KI im Unternehmen nutzen.

> **Keine Rechtsberatung.** Die Übersicht ordnet Pflichten ein; jede Entscheidung wird mit der eigenen Datenschutz- und Rechtsabteilung geklärt. Stand: 31.10.2026, vor Kursbeginn prüfen.

## Begriffe

| Begriff | Bedeutung |
| --- | --- |
| personenbezogene Daten | alle Angaben, die sich einer Person zuordnen lassen: Name, Mailadresse, Inhalt einer Mail über eine Person, Teilnahme an einer Besprechung. |
| Verantwortlicher | die Organisation, die über Zweck und Mittel einer Verarbeitung entscheidet, hier Nordwind, nicht Microsoft. |
| Auftragsverarbeitung | ein Dienstleister verarbeitet Daten im Auftrag und nach Weisung des Verantwortlichen; dafür ist ein Vertrag nötig (Art. 28 DSGVO). Wie ein Aktenvernichter, der nur nach Auftrag arbeitet. |
| Verzeichnis der Verarbeitungstätigkeiten | interne Liste aller Verarbeitungen mit Zweck, Datenarten, Betroffenen und Löschfristen (Art. 30 DSGVO). Das Inventar des Datenschutzes. |
| Datenschutz-Folgenabschätzung (DSFA) | vorab dokumentierte Prüfung von Risiken und Schutzmaßnahmen, wenn eine Verarbeitung voraussichtlich ein hohes Risiko für Personen hat (Art. 35 DSGVO). |
| besondere Kategorien | besonders geschützte Daten wie Gesundheit, Religion, Gewerkschaftszugehörigkeit, ethnische Herkunft (Art. 9 DSGVO). |
| EU AI Act | EU-Verordnung über künstliche Intelligenz (Verordnung (EU) 2024/1689); regelt KI nach Risiko, für Anbieter und für Organisationen, die KI einsetzen. |
| KI-Kompetenz | ausreichendes Wissen der Mitarbeitenden, um KI sachkundig einzusetzen und Chancen und Risiken zu kennen (Art. 4 EU AI Act). |
| Hochrisiko | Einstufung im EU AI Act für KI-Systeme in sensiblen Bereichen, z. B. Bewerberauswahl; mit strengen Pflichten. |
| Datenschutzbeauftragte | intern oder extern benannte Person, die berät, Verarbeitungen prüft und Ansprechstelle für die Aufsichtsbehörde ist; sie entscheidet nicht anstelle der Leitung. |

## DSGVO-Kern für Copilot

| Frage | Grundlage | Was für Copilot zu klären ist |
| --- | --- | --- |
| Wozu und auf welcher Rechtsgrundlage? | Art. 5, Art. 6 DSGVO | Zweck festlegen (z. B. Unterstützung bei Wissensarbeit, keine Leistungsbewertung); für Beschäftigtendaten zusätzlich nationale Regeln, Stand prüfen |
| Ist der Dienstleister vertraglich gebunden? | Art. 28 DSGVO | ob der Auftragsverarbeitungsvertrag mit Microsoft Copilot abdeckt; eigener Vertrag für jeden weiteren Dienst, z. B. externer MCP-Server |
| Ist die Verarbeitung dokumentiert? | Art. 30 DSGVO | Eintrag im Verzeichnis: Zweck, Datenarten (Mails, Chats, Dateien, Interaktionen), Betroffene, Löschfristen |
| Ist eine DSFA nötig? | Art. 35 DSGVO | prüfen und Ergebnis dokumentieren; Anlass: neue Technologie, viele Beschäftigtendaten, mögliche Rückschlüsse auf Verhalten |
| Wie lange bleiben Interaktionen und Memory? | Art. 5, Art. 17 DSGVO | Aufbewahrung und Löschung von Copilot-Interaktionen und Memory (Lab 1.2) festlegen |
| Sind besonders sensible Daten betroffen? | Art. 9 DSGVO | HR- und Gesundheitsdaten ausschließen oder gesondert schützen; ggf. lokales Modell |

## Was Microsoft zusagt

Laut Microsoft Learn (Stand: 31.10.2026, vor Kursbeginn prüfen):

- Prompts, Antworten und über Microsoft Graph gelesene Daten werden nicht zum Training der Basismodelle verwendet.
- Die Interaktionen (Prompt und Antwort) werden gespeichert und nach den vertraglichen Zusagen für die übrigen Microsoft-365-Inhalte verarbeitet.
- Für EU-Nutzende bleibt der Datenverkehr in der EU-Datengrenze (EU Data Boundary). Ausnahme laut derselben Seite: Modelle von Anthropic als Unterauftragsverarbeiter sind derzeit davon ausgenommen; welche Modelle im eigenen Tenant aktiv sind, ist zu prüfen.

_Quelle: Microsoft Learn, „Data, Privacy, and Security for Microsoft Copilot" (https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-privacy), abgerufen am 31.10.2026._

_Funktionsumfang hängt von Lizenz, Tenant-Einstellungen und Rollout ab; vor dem Kurs prüfen._

## Datenflüsse über Agenten und Anbindungen

Jede Anbindung aus Lab 2.3 kann einen neuen Datenweg und einen neuen Dienstleister bedeuten.

```text
Frage im Agenten
   │
   ├─ Microsoft 365 (Mails, Dateien)     → Microsoft, Auftragsverarbeitungsvertrag vorhanden?
   ├─ Konnektor zum CRM                  → Daten aus dem CRM werden in Microsoft 365 durchsuchbar
   ├─ MCP-Server eines Drittanbieters    → eigener Auftragsverarbeiter? eigener Vertrag? Serverstandort?
   └─ lokales Modell im eigenen Haus     → Daten verlassen das Haus nicht; Betrieb und Sicherheit intern
```

- Je Anbindung klären: welche Daten fließen, wer betreibt den Dienst, wo steht er, welcher Vertrag gilt.
- Für Daten nach Art. 9 DSGVO oder Geschäftsgeheimnisse kann ein lokales Modell die passende Option sein.

## EU AI Act

- **Art. 4 – KI-Kompetenz:** gilt seit 02.02.2025 für Anbieter und Betreiber, also auch für jede Organisation, die Copilot einsetzt. Mitarbeitende, die KI nutzen, brauchen eine passende Schulung; dokumentieren hilft beim Nachweis.
- Die Pflichten sind gestaffelt; Änderungen durch das EU-Gesetzespaket „Digital Omnibus" wurden vorgeschlagen. Stand prüfen.

| Risikoklasse | in einem Satz | Beispiel |
| --- | --- | --- |
| unannehmbares Risiko | verboten, seit 02.02.2025 | Emotionserkennung am Arbeitsplatz (Ausnahmen für Medizin und Sicherheit) |
| hohes Risiko | erlaubt mit strengen Pflichten (Risikomanagement, menschliche Aufsicht, Dokumentation) | Bewerberauswahl, Bewertung von Beschäftigten (Anhang III Nr. 4) |
| begrenztes Risiko | Transparenzpflichten | Chatbot muss als KI erkennbar sein; KI-erzeugte Inhalte kennzeichnen |
| minimales Risiko | keine zusätzlichen Pflichten | Rechtschreibhilfe, Spamfilter |

- Copilot für Mails, Berichte und Wissensfragen fällt in der Regel nicht unter Hochrisiko.
- Ein Agent, der Bewerbungen vorsortiert oder Mitarbeitende bewertet, kann Hochrisiko sein. Solche Fälle brauchen eine gesonderte Prüfung vor dem Bau.

## Rolle der Datenschutzbeauftragten

- berät früh, prüft Auftragsverarbeitung, Verzeichnis und DSFA, begleitet den Pilot,
- entscheidet nicht anstelle der Leitung; die Verantwortung bleibt beim Unternehmen,
- wird vor dem Pilot eingebunden, nicht nach dem Rollout.

## Grenzen

- Die Microsoft-Zusagen gelten für den Microsoft-Dienst, nicht für angebundene Drittsysteme oder private Werkzeuge (Schatten-KI aus Lab 3.1).
- Ein Vertrag ersetzt keine eigene Prüfung von Zweck, Berechtigungen und Löschung.

## Fazit

- Zweck, Auftragsverarbeitung, Verzeichnis, DSFA-Prüfung und Löschregeln sind vor dem Pilot zu klären.
- Jede Anbindung und jeder externe MCP-Server ist ein eigener Datenweg mit eigener Vertragsfrage.
- KI-Kompetenz ist seit 02.02.2025 Pflicht; Bewerberauswahl und Bewertung von Beschäftigten sind Hochrisiko-Bereiche.

In der Übung werden vier typische Irrtümer aufgelöst und der Compliance-Status von Nordwind geprüft.
