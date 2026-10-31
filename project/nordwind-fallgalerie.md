# Nordwind-Fallgalerie

Acht Anwendungsfälle aus der [Ausgangslage](nordwind-ausgangslage.md), verteilt auf drei Ausbaustufen. Grundlage für Lab 2.4. Alle Angaben sind fiktiv.

| Stufe | Bedeutung |
| --- | --- |
| 1 – Apps | Copilot in Outlook, Teams, Word, PowerPoint, Excel oder Copilot Chat, ohne eigene Einrichtung |
| 2 – Agent | eigener Agent mit Anweisungen und Wissensdateien bzw. Skills |
| 3 – Anbindung | Agent, der zusätzlich ein Fachsystem außerhalb von Microsoft 365 liest oder dort handelt |

## Fall A – Mailverläufe in Projekten

Projektleitungen erhalten täglich lange Mailverläufe mit Kunden und Unterauftragnehmern. Gesucht: Zusammenfassung mit offenen Punkten und ein Antwortentwurf. Nutzer: 160 Personen in der Beratung. Kontext: eigenes Postfach. **Stufe 1.**

## Fall B – Besprechungen nachbereiten

Nach Kundenterminen in Teams fehlen oft Aufgabenliste und Verantwortliche. Gesucht: Zusammenfassung mit Aufgaben. Nutzer: Beratung und Vertrieb. Kontext: Transkript der Besprechung (Transkription muss eingeschaltet sein). **Stufe 1.**

## Fall C – Monatsbericht Controlling

Controlling erstellt jeden Monat einen Bericht zu Projektbudgets aus Excel-Exporten. Gesucht: Auffälligkeiten und ein Diagramm. Nutzer: 15 Personen. Kontext: Excel-Tabellen in SharePoint. **Stufe 1.**

## Fall D – IT-Helfer

60 % der IT-Tickets betreffen dieselben zehn Themen (VPN, Passwort, Geräte). Gesucht: ein Agent, der Standardfragen aus der IT-Richtlinie beantwortet. Nutzer: alle Mitarbeitenden. Kontext: `nordwind-it-richtlinie.md`. **Stufe 2.**

## Fall E – Onboarding-Begleiter

Neue Mitarbeitende fragen in den ersten 30 Tagen immer wieder dasselbe. Das Vorgehen kennen nur zwei Personen in HR. Gesucht: ein Agent mit einer Skill-Datei für das Onboarding-Vorgehen. Nutzer: ca. 40 neue Mitarbeitende pro Jahr. Kontext: `nordwind-onboarding-leitfaden.md`, [Beispiel-Skill](skills/nordwind-onboarding-fragen/SKILL.md). **Stufe 2.**

## Fall F – Angebotsassistent

Der Vertrieb schreibt Angebote nach festen Regeln (Aufbau, Kalkulationsschema, Formulierungen), die nur erfahrene Personen beherrschen. Gesucht: ein Agent, der Angebotsentwürfe nach diesen Regeln erstellt. Nutzer: 25 Personen. Kontext: Angebotsvorlagen, Regeln als Skill-Datei. **Stufe 2.**

## Fall G – Kundenstatus aus dem CRM

Vor Kundenterminen wird der aktuelle Stand (offene Angebote, letzte Kontakte) aus dem CRM zusammengesucht. Gesucht: Abfrage in Teams, die das CRM liest. Nutzer: Vertrieb und Projektleitungen. Kontext: CRM, nur lesend. **Stufe 3.**

## Fall H – Tickets aus Mails anlegen

Support-Anfragen kommen per Mail und werden von Hand ins Ticketsystem übertragen. Gesucht: ein Agent, der aus einer Mail ein Ticket anlegt. Nutzer: IT. Kontext: Postfach und Ticketsystem, schreibend. **Stufe 3.**
