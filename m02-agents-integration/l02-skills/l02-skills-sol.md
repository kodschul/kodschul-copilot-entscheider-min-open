# Lab 2.2 – Lösung: KI baut KI: Skills und Markdown-Dateien

## Aufgabe 1: Menschliche Entscheidungen in der Kette

| Schritt | Entscheidung |
| --- | --- |
| 1 Problem-Solver | Das Problem ist das Vorgehen, das an zwei Personen hängt, nicht „ein Chatbot für HR"; die Top-Empfehlung wird angenommen. |
| 2 Solution Architect | Kein neuer Agent, sondern ein Skill im bestehenden Agenten; Gehalt und Vertrag bleiben bei HR. |
| 3 Skill-Generator | Entwurf gegen den Leitfaden prüfen; „Zugangsdaten per E-Mail" auf SMS korrigiert, erst dann freigegeben. |

## Aufgabe 2: Teile der `SKILL.md`

| Teil | Inhalt |
| --- | --- |
| `name` | `nordwind-onboarding-fragen` (gleich dem Ordnernamen) |
| `description` | Fragen neuer Mitarbeitender in den ersten 30 Tagen; ausdrücklich nicht für Gehalt, Vertrag, persönliche Ausnahmen |
| Vorgehen | vier Schritte: Thema zuordnen, nur aus Leitfaden/Richtlinie antworten, kurz mit nächstem Schritt, sonst an HR |
| Grenzen | kein Gehalt, Vertrag, Probezeitbewertung, persönliche Ausnahmen; keine Angaben über andere Personen |

## Aufgabe 3: Angaben geprüft

| Angabe im Beispiel | Fundstelle | Ergebnis |
| --- | --- | --- |
| Gerät eine Woche vor Start eingerichtet, per Kurier oder am ersten Tag | Onboarding-Leitfaden, „Vor dem ersten Arbeitstag" | belegt |
| Zugangsdaten für den Erstlogin per SMS | Onboarding-Leitfaden, „Vor dem ersten Arbeitstag" | belegt |
| IT-Support über das Ticket-Portal | IT-Richtlinie, „IT-Support-Kontakt" | belegt |

## Aufgabe 4: Wissensdatei oder Skill

- **Als Wissensdatei** (Weg der Demo): Der Agent durchsucht die Datei wie jedes Dokument; Vorgehen und Grenzen wirken nur, wenn die Suche sie zur Frage findet.
- **Als Skill** (wenn Lizenz und Tenant es erlauben): Der Agent lädt die Anleitung gezielt bei jeder Onboarding-Frage und hält Vorgehen und Grenzen verlässlicher ein.

## Aufgabe 5: Abschnitt 3 ergänzt

| Feld | Entwurf | Korrektur |
| --- | --- | --- |
| Erfahrungswissen | Vorgehen bei Fragen neuer Mitarbeitender in den ersten 30 Tagen | unverändert |
| Format | Markdown-Datei nach Skill-Format (`SKILL.md`) | unverändert |
| Owner | – | **HR (Onboarding)** |
| Prüfturnus | – | **halbjährlich und bei jeder Änderung von Onboarding-Leitfaden oder IT-Richtlinie** |

**Begründung:** HR kennt das Vorgehen und verantwortet den Leitfaden; ohne festen Turnus veraltet der Skill unbemerkt, und der Agent gibt veraltete Angaben mit Überzeugung weiter.

## Aufgabe 6: Zweiter Skill-Kandidat

**Angebotskalkulation nach Nordwind-Schema** (Vertrieb): Das Wissen steckt laut Ausgangslage bei wenigen langjährigen Personen, und Angebote entstehen jede Woche. Owner: Vertriebsleitung.

Vertretbar auch: Projektstart (Checkliste für neue Kundenprojekte, Owner: Projektleitung).

## Erweiterung

Ein brauchbarer Entwurf für die Angebotskalkulation hat eine `description` mit Ausschluss (z. B. „Nicht für Preisfreigaben"), ein Vorgehen ohne erfundene Preise und eine Grenze „Freigabe durch die Vertriebsleitung". Jede Zahl und Regel im Entwurf wird gegen die vorhandenen Angebotsunterlagen geprüft, bevor die Datei abgelegt wird.
