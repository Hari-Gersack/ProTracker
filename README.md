# ProTracker

Eine Web-App für das iPhone, mit der du deine tägliche Proteinzufuhr einträgst, ein Tagesziel verfolgst und Durchschnitte über beliebige Zeiträume auswertest. In einem separaten Trainingsbereich hältst du außerdem fest, wie sich deine Gewichte bei einzelnen Übungen entwickeln. Die App läuft komplett im Browser, funktioniert offline und lässt sich wie eine normale App auf den Home-Bildschirm legen.

## Protein

- **Heute:** Gramm eintragen. Die Uhrzeit steht automatisch auf „Jetzt“ und lässt sich ändern. Optional kannst du eine Notiz wie „Skyr“ dazuschreiben. Zuletzt genutzte Einträge erscheinen als Schnellauswahl. Mit den Pfeilen trägst du auch frühere Tage nach.
- **Shaker-Anzeige:** füllt sich bis zum Tagesziel.
- **Einträge bearbeiten:** Eintrag antippen, um Menge, Uhrzeit, Tag oder Notiz zu ändern oder ihn zu löschen.
- **Statistik:** Zeitraum 7 / 30 / 90 Tage oder frei wählbar. Angezeigt werden:
  - Durchschnitt pro Tag
  - Tage mit erreichtem Ziel
  - bester Tag und längste Serie
  - Verlauf mit 7-Tage-Schnitt
  - Auswertung nach Wochentag und nach Tageszeit
  - Tabelle aller Tage

## Training

Den Trainingsbereich öffnest du über den kleinen Knopf **Training** oben rechts auf der Seite „Heute“. Mit **‹ Protein** kommst du zurück.

- **Übungen anlegen:** z. B. Bankdrücken, Kniebeugen oder Klimmzüge. Häufige Übungen stehen als Vorschläge bereit.
- **Sätze eintragen:** Gewicht (kg) und Wiederholungen eingeben. Das Datum steht automatisch auf heute und lässt sich ändern. Die Werte vom letzten Satz bleiben stehen, für den nächsten Satz reicht also oft ein Tippen auf „Satz eintragen“. Übungen ohne Zusatzgewicht trägst du mit 0 kg ein.
- **Rekorde:** Ein Satz, der schwerer ist als alles davor, wird als „Rekord“ markiert.
- **Fortschritt:** Grafik über 1 Monat, 3 Monate, 1 Jahr, alles oder einen eigenen Zeitraum. Du kannst wählen, was angezeigt wird:
  - **Gewicht:** schwerster Satz pro Trainingstag
  - **1RM:** geschätztes Maximalgewicht für eine Wiederholung. Damit lassen sich Sätze mit unterschiedlich vielen Wiederholungen vergleichen.
  - **Wdh.:** meiste Wiederholungen in einem Satz
- **Verlauf:** alle Trainings mit ihren Sätzen. Einen Satz antippen, um ihn zu bearbeiten oder zu löschen.

Wenn die App im Studio zwischendurch neu lädt, öffnet sie wieder die Übung, an der du gerade warst. Nach drei Stunden startet sie wieder auf „Heute“.

## Auf GitHub Pages veröffentlichen

1. Auf [github.com](https://github.com) anmelden und oben rechts **+ → New repository** wählen.
2. Einen Namen vergeben, z. B. `protracker`, und **Public** auswählen. Dann **Create repository** klicken.
3. Auf der neuen Seite **uploading an existing file** wählen.
4. **Alle Dateien aus diesem Ordner** (nicht den Ordner selbst) ins Fenster ziehen. `index.html` muss also direkt im Hauptverzeichnis liegen.
5. Unten auf **Commit changes** klicken.
6. Im Repository **Settings → Pages** öffnen. Bei „Build and deployment“ als Source **Deploy from a branch** wählen, dann Branch **main** und Ordner **/ (root)**. Mit **Save** bestätigen.
7. Nach ein bis zwei Minuten ist die App erreichbar unter
   `https://DEIN-GITHUB-NAME.github.io/protracker/`

## Bestehende Version aktualisieren

Wenn die App schon online und auf deinem iPhone installiert ist:

1. Im Repository auf **Add file → Upload files** klicken.
2. Alle Dateien aus diesem Ordner hineinziehen. Gleichnamige Dateien werden dabei ersetzt.
3. Auf **Commit changes** klicken.
4. Die App auf dem iPhone mit Internet öffnen und einmal schließen und wieder öffnen. Danach ist die neue Version da.

Deine bisherigen Einträge bleiben erhalten, eine Neuinstallation ist nicht nötig.

## Auf dem iPhone installieren

1. Die Adresse in **Safari** öffnen.
2. Auf **Teilen** tippen (Quadrat mit Pfeil nach oben).
3. **Zum Home-Bildschirm** wählen und auf **Hinzufügen** tippen.

## Wichtig zu deinen Daten

- Alle Einträge werden **nur auf deinem iPhone** gespeichert. Nichts wird hochgeladen, auch nicht zu GitHub.
- Safari und die installierte App haben **getrennte Speicher**. Trag deine Daten deshalb nur in der installierten App ein.
- Wenn du die App vom Home-Bildschirm löschst, sind die Daten weg. Exportiere daher ab und zu unter **Einstellungen → Backup exportieren** eine Sicherung, z. B. in die Dateien-App oder iCloud Drive. Das Backup enthält Protein- und Trainingsdaten. Mit **Backup importieren** holst du alles zurück, auch auf ein neues iPhone.

## App später selbst ändern

Wenn du eine Datei änderst und neu hochlädst, erhöhe in `sw.js` die Versionsnummer in der Zeile `const CACHE = 'protracker-v2';` (z. B. auf `v3`). Dann lädt das iPhone beim nächsten Öffnen mit Internet die neue Version.

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
