# FAQ

**Sieht Copilot alle Dateien im Unternehmen?**
Nein. Copilot sieht nur, was die nutzende Person ohnehin öffnen darf. Ist ein Ordner für alle freigegeben, findet Copilot ihn aber für alle (Lab 1.1, 3.1).

**Werden Unternehmensdaten zum Training der KI verwendet?**
Laut Microsoft nicht: Prompts, Antworten und Daten aus Microsoft Graph werden nicht zum Training der Basismodelle genutzt (Stand: 31.10.2026, vor einer Entscheidung prüfen; Lab 1.1).

**Was ist der Unterschied zwischen Copilot Chat und Microsoft 365 Copilot?**
Copilot Chat ist ohne Zusatzlizenz nutzbar und arbeitet mit dem Web und hochgeladenen Dateien. Microsoft 365 Copilot ist eine Zusatzlizenz mit Copilot in den Apps und Zugriff auf die eigenen Arbeitsdaten (Lab 1.1).

**Warum liefert dieselbe Frage bei zwei Personen unterschiedliche Antworten?**
Weil der Kontext verschieden ist: andere Postfächer, Dateien, Berechtigungen und Memory-Einträge (Lab 1.2).

**Brauchen Agenten Programmierkenntnisse?**
Nein. Im Agent Builder entsteht ein Agent per Beschreibung oder Formular. Anspruchsvoll ist nicht die Technik, sondern gutes Wissen und klare Grenzen (Lab 2.1).

**Was ist der Unterschied zwischen einer Wissensdatei und einem Skill?**
Eine Wissensdatei enthält Fakten, die der Agent durchsucht. Ein Skill enthält eine Anleitung für eine Aufgabe und wird nur geladen, wenn die Aufgabe passt (Lab 2.2).

**Muss für jedes System eine eigene Anbindung gebaut werden?**
Mit MCP nicht: Ein System wird einmal als MCP-Server bereitgestellt und ist dann für jedes kompatible KI-Werkzeug nutzbar (Lab 2.3).

**Sollte ein Agent in Fachsystemen auch schreiben dürfen?**
Zunächst nur lesen. Schreibender Zugriff kommt nach Erfahrung im Pilot, mit Owner, Freigabe und Protokoll (Lab 2.3, 3.1).

**Was ist das größte Risiko bei der Einführung?**
In der Praxis meist Oversharing: zu weit gefasste Freigaben, die Copilot sichtbar macht. Danach folgen fehlerhafte Inhalte und Schatten-KI (Lab 3.1).

**Ist eine Datenschutz-Folgenabschätzung Pflicht?**
Das hängt vom Einsatz ab und wird mit der Datenschutzbeauftragten geprüft und dokumentiert; „nicht nötig" ohne Prüfung ist kein gültiges Ergebnis (Lab 3.2).

**Was verlangt der EU AI Act von Unternehmen, die Copilot nutzen?**
Unter anderem KI-Kompetenz der Mitarbeitenden (Art. 4, gilt seit 02.02.2025). Einsätze in Hochrisiko-Bereichen wie der Bewerberauswahl haben strengere Pflichten (Lab 3.2). Keine Rechtsberatung.

**Muss der Betriebsrat zustimmen?**
Bei technischen Einrichtungen, die Verhalten oder Leistung überwachen können, besteht in der Regel Mitbestimmung (§ 87 Abs. 1 Nr. 6 BetrVG); im öffentlichen Dienst gelten die Personalvertretungsgesetze. Einbinden vor dem Pilot (Lab 3.3). Keine Rechtsberatung.

**Ersetzt Copilot Arbeitsplätze?**
Aufgaben verändern sich, vor allem Suchen, Zusammenfassen und Entwerfen. Eine ehrliche Antwort, Schulung und Beteiligung wirken besser als Beschwichtigung (Lab 4.1).

**Wer sollte im Pilot sein?**
Eine gemischte Gruppe aus mehreren Bereichen, mit Begeisterten und Skeptischen, damit das Ergebnis übertragbar ist (Lab 4.2).

**Muss es immer der Cloud-Dienst sein?**
Nein. Für besonders schutzbedürftige Daten kommen auch self-hosted Plattformen mit lokalen Modellen infrage; oft ergänzen sich beide ([Ausblick](../m04-rollout/01-ausblick-betriebsmodelle.md)).
