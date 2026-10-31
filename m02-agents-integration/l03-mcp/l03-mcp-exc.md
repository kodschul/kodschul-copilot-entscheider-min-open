# Lab 2.3 – Übung: KI mit allem verbinden: MCP

**Ändert die Nordwind-Projektbasis?** Ja — Abschnitt 4 „Anbindung weiterer Systeme" in `nordwind-entscheidungsvorlage.md` wird geprüft und korrigiert.

## Abstimmung

Grundlage: Systemlandschaft in `../../project/nordwind-ausgangslage.md`. Die drei Fragen werden im Quiz-Werkzeug beantwortet oder allein notiert.

1. Welches System bindet Nordwind zuerst an? CRM / Ticketsystem IT / ERP / Buchhaltung
2. CRM: nur lesen oder auch schreiben?
3. ERP / Buchhaltung: Cloud-Modell, lokales Modell oder vorerst nicht anbinden?

## Ausgangslage: Beispiel aus der Demo

Ein KI-Werkzeug liest die Abstimmungsergebnisse über eine MCP-Anbindung an das Quiz-Werkzeug und fasst sie zusammen. Der MCP-Server des Quiz-Werkzeugs liefert diese Daten (Beispieldaten, Werte in Prozent):

```json
{
  "umfrage": "Nordwind-Systemlandschaft",
  "fragen": [
    {
      "frage": "Welches System zuerst anbinden?",
      "ergebnis": { "CRM": 55, "Ticketsystem IT": 35, "ERP / Buchhaltung": 10 }
    },
    {
      "frage": "CRM: nur lesen oder auch schreiben?",
      "ergebnis": { "nur lesen": 70, "lesen und schreiben": 30 }
    },
    {
      "frage": "ERP / Buchhaltung: welches Modell?",
      "ergebnis": { "Cloud-Modell": 20, "lokales Modell": 45, "vorerst nicht anbinden": 35 }
    }
  ]
}
```

Wichtig für die Prüfung sind nur die Felder `frage` und `ergebnis`; `umfrage` ist der Titel und kann ignoriert werden.

Der vom KI-Werkzeug formulierte Entwurf für Abschnitt 4:

> **Anbindung weiterer Systeme (Vorschlag aus der Abstimmung)**
>
> | System | Zuerst? | Zugriff | Modell |
> | --- | --- | --- | --- |
> | CRM | ja | lesen und schreiben | Cloud-Modell |
> | Ticketsystem IT | später | lesen | Cloud-Modell |
> | ERP / Buchhaltung | ja | lesen | lokales Modell (Mehrheit) |
>
> Die Gruppe spricht sich klar für eine schnelle Anbindung von CRM und ERP aus.

## Aufgaben

1. Notiere die eigenen Antworten auf die drei Abstimmungsfragen.
2. Vergleiche den Entwurf Zeile für Zeile mit den JSON-Daten. Notiere jede Angabe, die die Daten nicht stützen, mit dem richtigen Wert.
3. Prüfe, welche Angaben im Entwurf gar nicht abgefragt wurden (Annahmen des KI-Werkzeugs), und markiere sie als Annahme.
4. Öffne `../../project/nordwind-entscheidungsvorlage.md`, Abschnitt 4. Prüfe die Spalte „Zugriff" gegen die Regel „zuerst nur lesen" aus der Theorie.
5. Fülle die leere Spalte „Modell" je System aus: Cloud-Modell, lokales Modell oder vorerst keines. Begründe jede Zeile in wenigen Worten.
6. Trage für das CRM eine Prüffrage zum Betreiber des MCP-Servers unter der Tabelle ein.

## Checkpoint

- Mindestens zwei falsch übernommene Angaben aus dem KI-Entwurf sind mit richtigem Wert notiert.
- Abschnitt 4 hat keine leere Spalte mehr; der CRM-Zugriff ist auf Lesen begrenzt.
- Unter der Tabelle steht eine Betreiber-Prüffrage.

## Abschlusskriterien

- Abschnitt 4 nennt je System Reihenfolge, Zugriff und Modell mit kurzer Begründung.
- Der geprüfte Entwurf enthält keine Aussage mehr, die die Abstimmungsdaten nicht stützen.

## Fallback

Ohne MCP-Anbindung an das Quiz-Werkzeug: Ergebnisse als Datei exportieren und dem KI-Werkzeug als Datei geben, oder die Beispieldaten oben verwenden. Einschränkung: Das KI-Werkzeug liest dann einen festen Stand statt der aktuellen Ergebnisse.
