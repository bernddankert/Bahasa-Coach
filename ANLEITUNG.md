# Bahasa Indonesia Coach – iPhone-Installation

## Kostenlos mit HTTPS veröffentlichen (GitHub Pages)

1. Auf https://github.com ein Konto erstellen oder anmelden.
2. Ein **öffentliches** Repository erstellen, z. B. `bahasa-coach`.
3. **Alle Dateien und den Ordner `icons` aus diesem ZIP** ins Stammverzeichnis des Repositorys hochladen (nicht das ZIP als einzelne Datei).
4. Unter **Settings → Pages** bei **Build and deployment** die Quelle **Deploy from a branch** auswählen; Branch `main`, Ordner `/(root)`, speichern.
5. Nach der Veröffentlichung lautet die Adresse normalerweise `https://BENUTZERNAME.github.io/bahasa-coach/`. GitHub zeigt den genauen Link unter Pages an.
6. Diese Adresse auf dem iPhone **in Safari** öffnen → Teilen-Symbol → **Zum Home-Bildschirm** → Hinzufügen.

## Wichtig

- Die HTTPS-Adresse entsteht erst durch die Veröffentlichung auf GitHub Pages; sie kann nicht durch das ZIP allein erzeugt werden.
- Das Repository ist öffentlich, also auch der App-Quellcode und die mitgelieferten Lerninhalte. **Keine persönlichen Lerndaten oder Backups hochladen.**
- Lerndaten werden lokal im Browser gespeichert. Sie synchronisieren sich nicht automatisch zwischen Geräten. Vor einem Browserwechsel/Zurücksetzen den Lernstand exportieren.
- Der Offline-Modus funktioniert erst nach erfolgreichem ersten Online-Aufruf und Laden der Dateien. Browser-Sprachausgabe kann eine verfügbare indonesische Systemstimme bzw. Netzwerkverbindung benötigen.
- Für Aktualisierungen Dateien ersetzen und die Cache-Version in `service-worker.js` erhöhen.
