# Ausblick: Wohin die Reise geht – Cloud-Dienst oder eigene Plattform

Hintergrund zum Kursabschluss. Fasst zusammen, was aus Modul 1 und 2 für die nächsten Jahre folgt, und vergleicht zwei Betriebsmodelle als Entscheidungsgrundlage.

## Kontext wird unabhängig vom Anbieter

- **Kontext ist alles** (Lab 1.2): Die Qualität hängt weniger am Modell als an dem Wissen und den Systemen, mit denen die KI arbeitet.
- **Wissen als Markdown** (Lab 2.2): Anweisungen, Wissensdateien und Skills sind einfache Textdateien. Sie lassen sich versionieren und mit unterschiedlichen KI-Werkzeugen nutzen.
- **Anbindungen über MCP** (Lab 2.3): Ein Fachsystem wird einmal als MCP-Server bereitgestellt und ist dann für jedes kompatible KI-Werkzeug nutzbar.
- **Lokale KI-Modelle** (Lab 2.3): Offene Sprachmodelle laufen auch auf eigenen Servern; Daten verlassen das Haus dann nicht.

Zusammen ergibt das ein Architekturmuster: eine **Verbindungsschicht** zwischen Modellen, Unternehmenswissen und Fachsystemen.

```text
            Mitarbeitende (Chat, Teams, Fachanwendung)
                              │
                 ┌────────────┴────────────┐
                 │    Verbindungsschicht    │  Regeln, Berechtigungen, Protokoll
                 └──┬──────────┬────────┬──┘
                    │          │        │
            Modelle (Cloud  Wissen    Fachsysteme
            oder lokal)    (Markdown, (über MCP: CRM,
                            Dokumente) ERP, Tickets)
```

## Zwei Betriebsmodelle im Vergleich

| Kriterium | Cloud-Dienst (z. B. Microsoft 365 Copilot) | Self-hosted Plattform mit offenen Modellen |
| --- | --- | --- |
| Datenhaltung | beim Anbieter, im Rahmen seiner Zusagen (z. B. EU-Datengrenze) | im eigenen Rechenzentrum oder bei einem gewählten Hoster |
| Modellwahl | durch den Anbieter vorgegeben | frei wählbar, auch lokale Modelle |
| Integration in Microsoft 365 | tief, ohne eigene Entwicklung | über Schnittstellen, eigener Aufwand |
| Anbindung weiterer Systeme | über Konnektoren und Agenten des Anbieters | über eigene Anbindungen, z. B. MCP |
| Betriebsaufwand | gering, Lizenzkosten pro Person | eigener Betrieb oder Dienstleister, Infrastrukturkosten |
| Geeignet für | breite Nutzung im Arbeitsalltag | besonders schutzbedürftige Daten, Fachsysteme, Unabhängigkeit vom Anbieter |

Beide Modelle schließen sich nicht aus: Häufig nutzt die Breite der Belegschaft den Cloud-Dienst, während besonders schutzbedürftige Daten über eine eigene Plattform erschlossen werden.

## Referenzen

- Microsoft 365 Copilot als Cloud-Dienst: Lab 1.1 und Lab 3.2.
- Self-hosted Ansatz, Beispiel einer Umsetzung: Nextise CIP, beschrieben als self-hosted KI-Plattform auf Basis offener Modelle, die bestehende Systeme anbindet (Quelle: [nextise.de/firmen-ki](https://nextise.de/firmen-ki), abgerufen am 31.10.2026).

Stand: 31.10.2026. Angebote und Funktionen in diesem Bereich ändern sich schnell; vor einer Entscheidung aktuell prüfen.

Angewendet in Lab 4.2 (Ausbaustufen im 90-Tage-Plan).
