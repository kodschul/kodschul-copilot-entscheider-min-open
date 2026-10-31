# Lab 1.1: Was ist Copilot – und was passiert mit den Daten?

**Leitfragen:**

<details>
<summary>Wo geht im eigenen Bereich die meiste Zeit für Suchen, Lesen und Zusammenfassen verloren?</summary>

Typisch sind lange Mailverläufe, Besprechungen ohne Protokoll und Dateien, deren aktueller Stand unklar ist. Genau dort setzt ein KI-Assistent an: Er sucht, liest und fasst zusammen, der Mensch prüft und entscheidet.

</details>

<details>
<summary>Woher sollte ein Assistent wissen, was im Postfach einer Person steht?</summary>

Er braucht einen Zugang zu Mails, Chats, Terminen und Dateien dieser Person. Bei Microsoft 365 Copilot läuft dieser Zugang über eine Schnittstelle, die alle Microsoft-365-Daten einer Organisation verbindet (Microsoft Graph, siehe Begriffe).

</details>

<details>
<summary>Sollte ein Assistent mehr sehen dürfen als die Person, die ihn nutzt?</summary>

Nein. Copilot sieht nur, was die nutzende Person ohnehin öffnen darf. Daraus folgt aber auch: Was für zu viele Personen freigegeben ist, findet Copilot für alle diese Personen.

</details>

- Microsoft 365 Copilot verbindet ein Sprachmodell mit den Arbeitsdaten der jeweiligen Person.
- Copilot vergibt keine neuen Rechte; bestehende Berechtigungen gelten unverändert.
- Die Lizenzfrage ist eine Datenfrage: Copilot Chat ohne Arbeitsdaten, Microsoft 365 Copilot mit Arbeitsdaten.

## Copilot auf einen Blick

**Das Problem:** Wissen ist auf Mails, Chats, Besprechungen und Dateien verteilt. Wer eine Frage beantworten will, sucht, liest und fasst zusammen, bevor die eigentliche Arbeit beginnt.

**Das Bild:** Copilot ist ein Assistent mit dem **Schlüsselbund der jeweiligen Person**. Er kann jede Tür öffnen, zu der diese Person einen Schlüssel hat, aber keine andere. Steht eine Tür für alle offen, kommt auch der Assistent hinein.

**Definition:** Microsoft 365 Copilot ist ein KI-Assistent in den Microsoft-365-Apps (Outlook, Teams, Word, Excel, PowerPoint und eine eigene Chat-App). Er kombiniert ein Sprachmodell mit den Mails, Chats, Terminen und Dateien, auf die die nutzende Person Zugriff hat.

![Screenshot der Microsoft-365-Copilot-App mit Chat, Agents und Notebooks in der linken Leiste](https://support.microsoft.com/en-us/microsoft-365-copilot/media/one-copilot-hero.png)

_Quelle: Microsoft Support, „What is the Microsoft 365 Copilot app" (https://support.microsoft.com/en-us/microsoft-365-copilot/what-is-microsoft-copilot-app), abgerufen am 31.10.2026._

| Datum | Ereignis | Quelle |
| --- | --- | --- |
| 30.11.2022 | OpenAI veröffentlicht ChatGPT; generative KI wird für alle nutzbar | OpenAI (prüfen) |
| 16.03.2023 | Microsoft stellt Microsoft 365 Copilot vor | [Microsoft Blog](https://blogs.microsoft.com/blog/2023/03/16/introducing-microsoft-365-copilot-your-copilot-for-work/) |
| 01.11.2023 | allgemein verfügbar für Großkunden | Microsoft (prüfen) |
| Januar 2024 | verfügbar für Unternehmen jeder Größe | Microsoft (prüfen) |
| Januar 2025 | Copilot Chat für Microsoft-365-Konten ohne Zusatzlizenz | Microsoft (prüfen) |

**Verbreitung:** Microsoft gab im November 2024 an, dass fast 70 % der Fortune-500-Unternehmen Microsoft 365 Copilot nutzen; wie breit die Nutzung in diesen Unternehmen ist, nennt die Angabe nicht ([Microsoft News, 20.11.2024](https://news.microsoft.com/en-hk/2024/11/20/ignite-2024-why-nearly-70-of-the-fortune-500-now-use-microsoft-365-copilot/)). Aktuelle Zahlen vor dem Kurs prüfen.

**Beispiele und Anwendungsfälle:**

| Muster | Beispiel | Zeitgewinn entsteht durch |
| --- | --- | --- |
| Verdichten | 40 Mails eines Projektverlaufs in fünf Punkten | Lesezeit |
| Nachbereiten | Teams-Besprechung: Beschlüsse und Aufgaben | Protokollaufwand |
| Entwerfen | Statusbericht in Word aus Projektnotizen | Startpunkt statt leeres Blatt |
| Erklären | Excel-Tabelle befragen: „Wo liegt der größte Kostenblock?" | Einarbeitung |
| Suchen | „Was wurde mit dem Kunden zum Termin vereinbart?" | Suche über mehrere Ablageorte |

## Begriffe

| Begriff | Bedeutung |
| --- | --- |
| Sprachmodell | Programm, das aus sehr vielen Texten gelernt hat und die wahrscheinlich passende Fortsetzung eines Textes erzeugt. Wie eine extrem belesene Autovervollständigung: plausibel, aber nicht automatisch richtig. |
| Prompt | die Eingabe oder Frage an Copilot |
| Berechtigung | Recht einer Person, eine Mail, Datei oder einen Ordner zu öffnen; in Microsoft 365 über Freigaben geregelt. Der Schlüssel im Schlüsselbund. |
| Microsoft Graph | Schnittstelle, über die Copilot die Microsoft-365-Daten einer Person findet (Mails, Chats, Kalender, Dateien), immer mit deren Berechtigungen. Das Verzeichnis, in dem steht, welcher Schlüssel welche Tür öffnet. |
| Tenant | die Microsoft-365-Umgebung einer Organisation mit ihren Nutzerkonten, Daten und Einstellungen |
| Copilot Chat | KI-Chat für Microsoft-365-Konten ohne Zusatzlizenz; arbeitet mit dem Web und mit Dateien, die eine Person ausdrücklich hochlädt |
| Microsoft 365 Copilot | kostenpflichtige Zusatzlizenz; Copilot in den Apps und mit Zugriff auf die eigenen Arbeitsdaten über Microsoft Graph |
| EU-Datengrenze | Zusage von Microsoft, Daten von EU-Kunden innerhalb der EU zu speichern und zu verarbeiten |

## Berechtigungen gelten unverändert

| Situation | Was Copilot tut |
| --- | --- |
| Datei ist nur für die Projektleitung freigegeben | Copilot nutzt sie nur für die Projektleitung |
| Datei ist für „alle Mitarbeitenden" freigegeben | Copilot kann sie jeder Person als Quelle anzeigen |
| Person hat keinen Zugriff auf ein Postfach | Copilot liest dieses Postfach für sie nicht |

Bisher schützte oft nur, dass niemand eine Datei fand. Copilot findet sie. Die Ursache liegt in der Ablage, nicht im Werkzeug (vertieft in Lab 3.1).

> **Merksatz:** Copilot sieht, was die Person sehen darf – nicht mehr, aber auch nicht weniger.

## Copilot Chat oder Microsoft 365 Copilot?

| Kriterium | Copilot Chat | Microsoft 365 Copilot |
| --- | --- | --- |
| Lizenz | in vielen Microsoft-365-Abos enthalten | Zusatzlizenz je Person |
| Datenbasis | Web und ausdrücklich hochgeladene Dateien | zusätzlich Mails, Chats, Besprechungen, Dateien, Kalender |
| Ort | eigene Chat-App, in Teams und Outlook anheftbar | zusätzlich direkt in Word, Excel, PowerPoint, Outlook, Teams |
| Typische Nutzung | Formulieren, Recherche, Text zu einer Datei | Arbeit mit dem eigenen Arbeitskontext |

Entscheidungsfrage: Soll die Antwort die eigenen Mails, Termine und Dateien kennen? Dann braucht es Microsoft 365 Copilot. Produktnamen und Lizenzzuschnitte ändern sich häufig; die Microsoft-Dokumentation nennt das Produkt inzwischen teils „Microsoft Copilot".

## Was passiert mit den Daten?

| Frage | Aussage von Microsoft |
| --- | --- |
| Wo werden Daten verarbeitet? | im Microsoft-365-Dienst des Tenants, unter denselben Vertragszusagen wie Mails und Dateien |
| Werden Daten zum Training genutzt? | Prompts, Antworten und über Microsoft Graph gelesene Daten werden nicht zum Training der Basismodelle genutzt |
| Bleiben Daten in der EU? | für EU-Kunden ist Copilot ein Dienst innerhalb der EU-Datengrenze; Ausnahme laut Microsoft: Modelle des Anbieters Anthropic, die als Unterauftragsverarbeiter eingebunden sind (prüfen) |
| Wird etwas gespeichert? | Prompts und Antworten werden als Verlauf gespeichert, verschlüsselt und wie andere Microsoft-365-Inhalte behandelt |

Quelle: Microsoft Learn, [Data, Privacy, and Security for Microsoft Copilot](https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-privacy) (Seitenstand 09.07.2026). Stand: 31.10.2026. Funktionsumfang hängt von Lizenz, Tenant-Einstellungen und Rollout ab; vor dem Kurs prüfen.

## Grenzen

- Ein Sprachmodell erzeugt plausiblen Text, keine geprüften Fakten; Zahlen, Namen und Fristen können falsch sein, auch wenn eine Quelle genannt ist.
- Ohne passende Daten bleibt die Antwort allgemein; eine Fehlermeldung gibt es dafür nicht.
- Die Zusagen zur Datenverarbeitung ersetzen keine eigene Prüfung durch Datenschutz und Mitarbeitervertretung (Modul 3).

## Fazit

- Copilot = Sprachmodell + Arbeitsdaten der Person, über Microsoft Graph und nur mit deren Berechtigungen.
- Zu weit freigegebene Dateien werden durch Copilot sichtbar; das ist eine Ablagefrage.
- Copilot Chat und Microsoft 365 Copilot unterscheiden sich in der Datenbasis, nicht im Prinzip.
- Microsoft sagt zu: kein Training mit Kundendaten, Verarbeitung in der EU-Datengrenze; Stand vor jeder Entscheidung prüfen.

Die Übung löst das Einstiegsquiz vom Anfang des Labs mit dieser Theorie auf.
