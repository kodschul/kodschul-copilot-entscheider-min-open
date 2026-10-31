# Lab 3.1: Risiken erkennen und begrenzen

**Leitfragen:**

<details>
<summary>Welche Ordner im eigenen Unternehmen sind vermutlich für mehr Personen freigegeben als nötig?</summary>

Typisch sind über Jahre gewachsene Projekt-, Angebots-, HR- und Finanzordner mit der Freigabe „alle Mitarbeitenden". Copilot macht genau diese Dateien leicht auffindbar, weil es alles nutzt, was die fragende Person sehen darf (Lab 1.1).

</details>

<details>
<summary>Wer haftet für einen Text, den ein Assistent geschrieben hat?</summary>

Die Person bzw. Organisation, die den Text freigibt und verwendet. Ein Werkzeug kann einen Fehler erzeugen, aber keine Verantwortung übernehmen.

</details>

<details>
<summary>Was passiert, wenn das freigegebene Werkzeug schlechter ist als das private?</summary>

Mitarbeitende weichen auf private KI-Werkzeuge aus, oft mit Firmen- oder Kundendaten. Verbote allein helfen wenig; ein brauchbares freigegebenes Werkzeug plus klare Regeln wirkt besser.

</details>

- Copilot schafft kaum neue Risiken, macht aber vorhandene sichtbar: Was zu weit freigegeben ist, wird jetzt gefunden.
- Jeder Agent, jeder Skill, jeder Konnektor und jeder MCP-Server aus Modul 2 erweitert die Fläche, über die Daten erreichbar sind.
- Gegenmaßnahmen sind überwiegend Führungsentscheidungen, keine Technikfragen.

## Begriffe

| Begriff | Bedeutung |
| --- | --- |
| Oversharing | Dateien oder Ordner sind für mehr Personen freigegeben, als sie brauchen. Bild: ein Aktenschrank auf dem Flur, der nie abgeschlossen wurde. |
| Schatten-KI | KI-Werkzeuge, die Mitarbeitende ohne Freigabe der Organisation nutzen, z. B. private Chat-Konten. Wie private USB-Sticks für Firmendaten. |
| Vertraulichkeitskennzeichnung | Markierung einer Datei oder Mail als z. B. „öffentlich", „intern", „vertraulich"; Microsoft 365 kann daran Schutzregeln knüpfen (Verschlüsselung, Weitergabe). Wie ein Stempel „Vertraulich" auf einer Akte, der auch technisch wirkt. |
| KI-Richtlinie | kurzes internes Regelwerk: welche KI-Werkzeuge erlaubt sind, welche Daten tabu sind, was vor der Weitergabe geprüft wird, wohin Probleme gemeldet werden. |
| Prüfpflicht | Regel, dass KI-Ergebnisse vor Weitergabe oder Entscheidung von einem Menschen geprüft werden. |
| Risikomatrix | Tabelle, die jedes Risiko nach Eintrittswahrscheinlichkeit und Auswirkung einordnet, damit klar wird, was zuerst behandelt wird. |

## Fünf Risikoklassen

| # | Risiko | Woran es sich zeigt | Beispiel Nordwind | Gegenmaßnahme |
| -: | --- | --- | --- | --- |
| 1 | fehlerhafte oder erfundene Inhalte | Zahl, Termin oder Quelle lässt sich nicht auf ein Originaldokument zurückführen | erfundener Starttermin in einem Kundenbericht | Prüfpflicht vor Versand; Quellenangaben in der Antwort nutzen |
| 2 | Oversharing | Copilot zitiert Dateien, die die fragende Person nie hätte finden sollen | Angebotskalkulationen sind für „alle Mitarbeitenden" freigegeben | Freigaben vor dem Rollout prüfen, sensible Dateien kennzeichnen |
| 3 | Schatten-KI | Firmen- oder Kundendaten landen in privaten Werkzeugen ohne Vertrag | ein Drittel der Belegschaft nutzt private KI-Werkzeuge, teils mit Kundendaten | freigegebenes Werkzeug anbieten, KI-Richtlinie, Meldeweg |
| 4 | Abhängigkeit und Kompetenzverlust | niemand kann ein Ergebnis mehr selbst nachrechnen oder einordnen | Angebote entstehen nur noch per Agent, die Kalkulationslogik kennt keiner mehr | Ergebnis verstehen statt übernehmen; Wissen als Skill dokumentieren (Lab 2.2) |
| 5 | Kosten ohne Nutzung | Lizenzen sind bezahlt, aber kaum genutzt | Lizenzen für alle, nach drei Monaten nutzt die Hälfte Copilot nie | Lizenzen nach Nutzung vergeben, Nutzung nach 60 Tagen auswerten |

> **Merksatz:** Ein Werkzeug kann einen Fehler erzeugen, aber niemals die Verantwortung dafür übernehmen.

## Oversharing: das größte reale Risiko

Copilot vergibt keine neuen Rechte. Es durchsucht über Microsoft Graph (Lab 1.1) alles, was die fragende Person ohnehin öffnen dürfte. Bisher schützte oft nur, dass niemand die Datei fand.

```text
Ordner "Angebote 2019-2026"  ── Freigabe: alle Mitarbeitenden
        │
 bisher:  Datei liegt in Unterordner 14, niemand sucht dort      → praktisch unsichtbar
 mit Copilot:  "Welche Tagessätze kalkulieren wir für Stadtwerke?"
               → Antwort mit Zitat aus der Kalkulation            → für alle sichtbar
```

- Die Ursache liegt in der Ablage, nicht in Copilot; die Lösung auch: Freigaben prüfen und einschränken, bevor die erste Lizenz vergeben wird.
- Vertraulichkeitskennzeichnungen helfen, sensible Dateien zu schützen, auch wenn eine Freigabe zu weit ist. In Microsoft 365 geschieht das über Microsoft Purview (Werkzeugname als Beispiel).
- Freigabeberichte zeigen, welche Orte für „alle" oder für Externe offen sind; Umfang und Lizenzbedarf sind tenant-abhängig.

_Stand: 31.10.2026. Funktionsumfang hängt von Lizenz, Tenant-Einstellungen und Rollout ab; vor dem Kurs prüfen._

## Agenten, Skills und Anbindungen als Zugriffsfläche

Jede Erweiterung aus Modul 2 öffnet einen weiteren Weg zu Daten oder Handlungen. Deshalb braucht jede einen Owner, eine Freigabe und ein Review.

| Erweiterung (aus Lab) | Was zusätzlich geprüft wird |
| --- | --- |
| geteilter Agent (2.1) | für welche Nutzergruppe freigegeben, welches Wissen enthalten, wer ihn abschaltet |
| Skill / Wissensdatei (2.2) | ob die Anleitung stimmt, wer sie pflegt, ob sie versteckte Regeln oder Entscheidungen enthält |
| Konnektor (2.3) | welche Daten aus dem Fremdsystem durchsuchbar werden, für wen |
| MCP-Server (2.3) | wer ihn betreibt, nur lesen oder auch schreiben, welche Funktionen und Daten erreichbar sind |

| Feld je Erweiterung | Zweck |
| --- | --- |
| Owner | benannte Person, die verantwortlich ist und Fragen beantwortet |
| Freigabe | Prüfung vor dem Teilen oder Anbinden |
| Review-Turnus | regelmäßige Prüfung, ob Inhalt und Rechte noch stimmen |
| Abschaltkriterium | wann ein Agent, Skill oder eine Anbindung beendet wird |

## Gegenmaßnahmen auf Entscheiderebene

| Maßnahme | wirkt vor allem gegen | typisch verantwortlich |
| --- | --- | --- |
| Berechtigungen und Freigaben vor dem Rollout prüfen | Oversharing | IT mit den Bereichsleitungen |
| Vertraulichkeitskennzeichnungen einführen | Oversharing | IT, Datenschutz |
| Prüfpflicht für Ergebnisse vor Weitergabe | fehlerhafte Inhalte | Führungskräfte der Bereiche |
| KI-Richtlinie in einfacher Sprache | Schatten-KI, fehlerhafte Inhalte | Geschäftsführung |
| Regeln für Bau und Freigabe von Agenten und Skills | Zugriffsfläche, Kompetenzverlust | IT, Fachbereiche |
| Lizenzvergabe nach Nutzung | Kosten ohne Nutzung | IT, Controlling |

## Risikomatrix

Jedes Risiko erhält eine Eintrittswahrscheinlichkeit und eine Auswirkung (niedrig, mittel, hoch). Was oben rechts steht, wird zuerst behandelt.

| Wahrscheinlichkeit ↓ / Auswirkung → | niedrig | mittel | hoch |
| --- | --- | --- | --- |
| **hoch** | beobachten | vor dem Pilot behandeln | **vor dem Pilot behandeln, Pilot sonst nicht starten** |
| **mittel** | akzeptieren | Maßnahme im Pilot | vor dem Pilot behandeln |
| **niedrig** | akzeptieren | beobachten | Maßnahme im Pilot |

- Jedes Risiko bekommt eine konkrete Gegenmaßnahme und eine verantwortliche Rolle, keine Person „irgendwer".
- Die Bewertung ist eine begründete Einschätzung, keine Messung; sie wird nach dem Pilot überprüft.

## Grenzen

- Eine Risikomatrix ersetzt keine Datenschutz- oder Rechtsprüfung (Lab 3.2) und keine Einbindung der Mitarbeitervertretung (Lab 3.3).
- Werkzeuge wie Kennzeichnungen und Freigabeberichte wirken nur, wenn jemand sie pflegt.

## Fazit

- Oversharing und Schatten-KI sind die beiden Risiken, die bei den meisten Organisationen schon vor Copilot bestehen.
- Jede Erweiterung (Agent, Skill, Konnektor, MCP-Server) braucht Owner, Freigabe und Review.
- Jedes Risiko erhält eine Gegenmaßnahme und eine verantwortliche Rolle.

In der Übung entsteht die Risikomatrix für den Nordwind-Top-Fall, und eine KI-Zusammenfassung mehrerer Matrizen wird geprüft.
