# Lab 3.3: Betriebsrat und Personalrat einbinden

**Leitfragen:**

<details>
<summary>Wann wurde die Mitarbeitervertretung bei der letzten Softwareeinführung eingebunden – und war das früh genug?</summary>

Oft erst, als der Vertrag unterschrieben war. Bei Werkzeugen, die Daten über Mitarbeitende erzeugen, verzögert eine späte Einbindung den Start meist mehr als eine frühe.

</details>

<details>
<summary>Welche Sorge hätten Mitarbeitende, wenn ein Assistent alle Mails und Besprechungen kennt?</summary>

Dass die Führung mitliest, auswertet, wer wie arbeitet, oder Fehler und Fragen gegen sie verwendet. Genau diese Sorge regelt eine Vereinbarung.

</details>

<details>
<summary>Welche Auswertungen über die Nutzung sollte die Führung bewusst nicht sehen?</summary>

Auswertungen einzelner Personen: wer wie oft fragt, was gefragt wurde, Inhalte aus Memory oder Interaktionsverlauf. Zusammengefasste Nutzungszahlen je Gruppe reichen für die Steuerung.

</details>

- Copilot erzeugt Daten über Nutzung und Verhalten; damit ist die Mitarbeitervertretung in der Regel zu beteiligen.
- Früh einbinden spart Zeit: Eine Pilotvereinbarung vor dem Start ist schneller als eine Genehmigung im Nachhinein.
- Die Vereinbarung beantwortet die Sorgen der Mitarbeitenden schriftlich und schafft Akzeptanz.

> **Keine Rechtsberatung.** Die Übersicht ordnet die Rechtslage ein; die konkrete Bewertung erfolgt mit der eigenen Rechtsabteilung oder Fachanwälten. Stand: 31.10.2026, vor Kursbeginn prüfen.

## Begriffe

| Begriff | Bedeutung |
| --- | --- |
| Mitarbeitervertretung | gewählte Vertretung der Beschäftigten: Betriebsrat oder Personalrat. |
| Betriebsrat | Mitarbeitervertretung in privatwirtschaftlichen Betrieben, geregelt im Betriebsverfassungsgesetz (BetrVG). |
| Personalrat | Mitarbeitervertretung im öffentlichen Dienst, geregelt im Bundespersonalvertretungsgesetz (BPersVG) bzw. in den Personalvertretungsgesetzen der Länder. |
| Mitbestimmung | Recht der Mitarbeitervertretung, bei bestimmten Maßnahmen gleichberechtigt mitzuentscheiden: Ohne Einigung darf die Maßnahme nicht umgesetzt werden. |
| Betriebsvereinbarung / Dienstvereinbarung | schriftlicher Vertrag zwischen Arbeitgeber und Betriebsrat bzw. Dienststelle und Personalrat, der für alle Beschäftigten verbindlich gilt. Wie eine Hausordnung, die beide Seiten unterschreiben. |
| Pilotvereinbarung | befristete Vereinbarung für eine Testphase mit kleiner Gruppe; wird nach der Auswertung angepasst oder durch eine dauerhafte ersetzt. |
| Einigungsstelle | Schlichtungsgremium, das entscheidet, wenn sich Arbeitgeber und Betriebsrat in einer mitbestimmungspflichtigen Frage nicht einigen. |

## Warum Copilot mitbestimmungspflichtig sein kann

§ 87 Abs. 1 Nr. 6 BetrVG: Der Betriebsrat bestimmt mit bei der „Einführung und Anwendung von technischen Einrichtungen, die dazu bestimmt sind, das Verhalten oder die Leistung der Arbeitnehmer zu überwachen".

- Der Wortlaut sagt „dazu bestimmt"; nach ständiger Rechtsprechung des Bundesarbeitsgerichts genügt aber, dass eine Einrichtung objektiv **geeignet** ist, Verhalten oder Leistung zu überwachen. Eine Überwachungsabsicht ist nicht nötig.
- Copilot ist in diesem Sinn in der Regel geeignet: Nutzungsberichte, Interaktionsverlauf, Memory und Besprechungstranskripte erzeugen Daten über einzelne Personen.
- Folge: Ohne Einigung mit dem Betriebsrat darf Copilot nicht eingeführt werden; ohne Einigung entscheidet die Einigungsstelle (§ 87 Abs. 2 BetrVG).

| Grundlage | Inhalt | Bedeutung für Copilot |
| --- | --- | --- |
| § 87 Abs. 1 Nr. 6 BetrVG | Mitbestimmung bei technischen Einrichtungen zur Verhaltens- und Leistungsüberwachung | Kern der Mitbestimmung |
| § 90 Abs. 1 Nr. 3 BetrVG | rechtzeitige Unterrichtung bei der Planung von Arbeitsverfahren einschließlich des Einsatzes von Künstlicher Intelligenz | Information schon in der Planungsphase |
| § 80 Abs. 3 BetrVG | Betriebsrat darf einen Sachverständigen hinzuziehen; bei der Beurteilung von KI gilt das als erforderlich | Kosten und Zeit für einen Sachverständigen einplanen |
| § 80 Abs. 1 Nr. 21 BPersVG | Mitbestimmung des Personalrats bei technischen Einrichtungen zur Verhaltens- oder Leistungsüberwachung (Bundesbehörden) | entspricht § 87 Abs. 1 Nr. 6 BetrVG |
| Personalvertretungsgesetze der Länder | Landes- und Kommunalverwaltungen; Regelungen weichen voneinander ab | das jeweilige Landesgesetz prüfen |

_Quellen: BetrVG (https://www.gesetze-im-internet.de/betrvg/), BPersVG (https://www.gesetze-im-internet.de/bpersvg_2021/), abgerufen am 31.10.2026._

## Früh einbinden statt nachträglich genehmigen

```text
Planung ──► Information ──► Pilotvereinbarung ──► Pilot ──► Auswertung ──► Betriebs-/Dienstvereinbarung ──► Rollout
   │            │                  │                                │
   │            └ § 90 BetrVG:     └ Regeln für Testgruppe          └ gemeinsame Auswertung
   │              rechtzeitig        und Zeitraum                     mit der Mitarbeitervertretung
   └ Mitarbeitervertretung sitzt mit am Tisch (z. B. in der Projektgruppe)
```

- Information nach dem Pilot ist zu spät: Schon der Pilot nutzt eine technische Einrichtung mit Mitarbeitenden.
- Eine Pilotvereinbarung auf Probe erlaubt einen schnellen Start und sammelt Erfahrungen für die dauerhafte Vereinbarung.
- Eine Betriebsvereinbarung kann zugleich Rechtsgrundlage für die Verarbeitung von Beschäftigtendaten sein (Art. 88 DSGVO); der EuGH hat die Anforderungen daran 2023 präzisiert (Urteil C-34/21), Stand mit dem Datenschutz prüfen. Bezug zum Datenschutz aus Lab 3.2.

## Typische Inhalte einer Betriebs- oder Dienstvereinbarung

| Baustein | Typische Regelung |
| --- | --- |
| Zweck und Geltungsbereich | welche Werkzeuge (Copilot in den Apps, Agenten), welche Gruppen, welcher Zweck (Unterstützung der Arbeit) |
| keine Leistungs- und Verhaltenskontrolle | Copilot-Daten werden nicht zur Bewertung einzelner Personen und nicht für arbeitsrechtliche Maßnahmen verwendet |
| Nutzungsberichte | nur zusammengefasst ab einer Mindestgruppengröße, keine Auswertung einzelner Personen; wer sie sieht |
| Interaktionsverlauf und Memory | wer Zugriff hat, Löschfristen, Memory für Nutzende sichtbar und löschbar |
| Besprechungen | Transkription und Mitschnitt nur angekündigt und mit Zustimmung der Teilnehmenden |
| Agenten mit Personenbezug | Agenten, die über Personen Auskunft geben oder Entscheidungen über sie vorbereiten, nur nach gesonderter Zustimmung |
| Schulung | Anspruch auf Schulung vor der Nutzung (Bezug: KI-Kompetenz, Lab 3.2) |
| Evaluierung und Anpassung | gemeinsame Auswertung nach festem Zeitraum, Anpassung bei neuen Funktionen |

## Grenzen

- Ob und wie weit Mitbestimmung greift, hängt vom Einzelfall und vom Funktionsumfang ab, der sich häufig ändert.
- Neue Copilot-Funktionen können eine bestehende Vereinbarung überholen; eine Anpassungsklausel ist daher wichtig.

## Fazit

- Copilot ist in der Regel geeignet, Verhalten oder Leistung zu überwachen; damit greift die Mitbestimmung.
- Die Mitarbeitervertretung gehört in die Planung, nicht in die Nachbereitung.
- Eine Pilotvereinbarung auf Probe ermöglicht einen schnellen, abgesicherten Start.

In der Übung entstehen die Eckpunkte einer Nordwind-Vereinbarung und eine Antwort auf die erwartete Sorge.
