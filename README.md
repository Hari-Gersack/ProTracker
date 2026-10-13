# Protein-Tracker

Eine Web-App für das iPhone, mit der du deine tägliche Proteinzufuhr einträgst, ein Tagesziel verfolgst und Durchschnitte über beliebige Zeiträume auswertest. Sie läuft komplett im Browser, funktioniert offline und lässt sich wie eine normale App auf den Home-Bildschirm legen.

## Funktionen

- **Heute:** Gramm eintragen, Uhrzeit steht automatisch auf „Jetzt“ und lässt sich ändern. Optional eine Notiz wie „Skyr“. Zuletzt genutzte Einträge erscheinen als Schnellauswahl. Mit den Pfeilen kannst du auch frühere Tage nachtragen.
- **Shaker-Anzeige:** füllt sich bis zum Tagesziel.
- **Einträge bearbeiten:** Eintrag antippen, um Menge, Uhrzeit, Tag oder Notiz zu ändern oder ihn zu löschen.
- **Statistik:** Zeitraum 7 / 30 / 90 Tage oder frei wählbar (z. B. 13.10.2026 bis 13.12.2026). Angezeigt werden:
  - Durchschnitt pro Tag
  - Tage mit erreichtem Ziel
  - bester Tag und längste Serie
  - Verlauf mit 7-Tage-Schnitt
  - Auswertung nach Wochentag und nach Tageszeit
  - Tabelle aller Tage
- **Einstellungen:** Tagesziel ändern. Vergangene Tage behalten ihr damaliges Ziel, wenn du es nicht anders auswählst. Außerdem Backup exportieren und importieren.

## Auf GitHub Pages veröffentlichen

1. Auf [github.com](https://github.com) anmelden und oben rechts **+ → New repository** wählen.
2. Einen Namen vergeben, z. B. `protein`, und **Public** auswählen. Dann **Create repository** klicken.
3. Auf der neuen Seite auf **uploading an existing file** klicken.
4. **Alle Dateien aus diesem Ordner** (nicht den Ordner selbst) in das Fenster ziehen. `index.html` muss also direkt im Hauptverzeichnis liegen.
5. Unten auf **Commit changes** klicken.
6. Im Repository **Settings → Pages** öffnen. Bei „Build and deployment“ als Source **Deploy from a branch** wählen, dann Branch **main** und Ordner **/ (root)**. Mit **Save** bestätigen.
7. Nach ein bis zwei Minuten ist die App erreichbar unter
   `https://DEIN-GITHUB-NAME.github.io/protein/`

## Auf dem iPhone installieren

1. Die Adresse in **Safari** öffnen.
2. Auf **Teilen** tippen (Quadrat mit Pfeil nach oben).
3. **Zum Home-Bildschirm** wählen und auf **Hinzufügen** tippen.

Danach startet die App vom Home-Bildschirm im Vollbild, mit eigenem Icon und auch ohne Internet.

## Wichtig zu deinen Daten

- Alle Einträge werden **nur auf deinem iPhone** gespeichert (im lokalen Speicher der App). Nichts wird hochgeladen, auch nicht zu GitHub.
- Safari und die installierte App haben **getrennte Speicher**. Trag deine Daten deshalb nur in der installierten App ein.
- Wenn du die App vom Home-Bildschirm löschst, sind die Daten weg. Exportiere daher ab und zu unter **Einstellungen → Backup exportieren** eine Sicherung, z. B. in die Dateien-App oder iCloud Drive. Mit **Backup importieren** holst du sie zurück, auch auf ein neues iPhone.

## App später ändern

Wenn du eine Datei änderst und neu hochlädst, erhöhe in `sw.js` die Versionsnummer in der Zeile `const CACHE = 'protein-tracker-v1';` (z. B. auf `v2`). Dann lädt das iPhone beim nächsten Öffnen mit Internet die neue Version. Deine Einträge bleiben dabei erhalten.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App (Oberfläche und Logik) |
| `manifest.json` | Name, Farben und Icons für den Home-Bildschirm |
| `sw.js` | Service Worker für den Offline-Betrieb |
| `apple-touch-icon.png` | Icon für den iPhone-Home-Bildschirm |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Icons für Android und andere Browser |
| `favicon-32.png` | Symbol im Browser-Tab |
| `nunito.woff2` | Ersatzschrift für Nicht-Apple-Geräte (Open Font License) |
