# Didaktischer Qualitätsaudit – Bahasa Coach 23.0

## Prüfungsumfang und Methode
Statische Auswertung der **48 ursprünglichen Kernkapitel** mit **576 ursprünglichen Kartenpaaren** (die später dynamisch angefügten Zusatzkapitel und Zusatzlexika sind in diesen Zählungen **nicht enthalten**). Überprüfung von Lernziel-Feldern, Grammatikregel-Feldern, Dubletten, Mehrfachübersetzungen und der tatsächlichen Bewertungslogik im Quellcode. Keine Muttersprachlerprüfung, keine wissenschaftliche Korpusvalidierung und keine Behauptung eines vollständigen A1–B2-CEFR-Audits.

## Messwerte
- Ursprüngliche Kapitel ohne formuliertes Lernziel: **0**.
- Ursprüngliche Kapitel ohne Grammatikfeld: **0**.
- Exakt wiederholte Deutsch-Indonesisch-Paare in Kernkapiteln: **37**.
- Deutsche Ausdrücke mit mehreren indonesischen Übersetzungen in Kernkapiteln: **5**; diese Fälle sind **Prüfkandidaten, nicht automatisch Fehler**.

## Bestätigte didaktische Probleme im Programmcode
1. **Grammatiktraining prüfte ursprünglich nur Textgleichheit** (`norm(answer)===norm(x.id)`). Das bestraft korrekte Paraphrasen und misst Satzübersetzung statt der angekündigten konkreten Grammatikkompetenz.
2. **Grammatikaufgaben** wurden aus beliebigen als „Satz“ klassifizierten Karten des Kapitels gewählt; die Passung zur Regel wurde nicht automatisch überprüft.
3. **Fortschrittszahlen** konnten exakte Musterlösungen mit echter sprachlicher Beherrschung verwechseln.
4. **Audio** hängt von der iOS-Systemstimme ab; technische Unterstützung ist kein Nachweis für indonesische Aussprachequalität.
5. **Zusatzkapitel und Vokabelerweiterungen** wurden in mehreren Versionen addiert, ohne dass für alle ein nachvollziehbarer Kompetenznachweis oder Muttersprachlerreview vorliegt.

## Sofort umgesetzte Verbesserungen in v23
- Lernziel, Regel und aktiver Transferimpuls werden vor der Grammatikübung deutlicher angezeigt.
- Bei Grammatikantworten wird zuerst die Musterlösung gezeigt, dann bewertet der Lernende die inhaltliche Korrektheit selbst. **Keine unzuverlässige automatische Falschbewertung mehr.**
- Selbstbewertung wird separat als solche gekennzeichnet und gespeichert; alte Lernstände werden nicht gelöscht.
- Kleine Lernsequenz mit explizitem Abrufen, Rückmeldung und Transfer.

## Offene Qualitätsarbeiten
- Alle zusätzlichen Karten und Kapitel exportieren und **einzeln** gegen zuverlässige indonesische Wörterbücher und Muttersprachlerurteile prüfen.
- CEFR-Kompetenzraster A1–B2 je Kapitel, mit prüfbaren „Kann“-Aussagen und echten produktiven Aufgaben.
- Aufgaben-Pool mit nachgewiesener Regelpassung; Grammatik darf nicht bloss Vokabelübersetzung sein.
- Externe Hördateien mit nachgewiesener Aussprachequalität statt ausschliesslich Geräte-TTS.
- FSRS-Datenmodell und Wiederholungslogik durch reproduzierbare Tests validieren.
