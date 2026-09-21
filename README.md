# 🦕 Spardino – Budget-Planer & Sparziele

Eine kleine Web-App mit zwei Bereichen, die du unten per Tab wechselst:

- **Planer**: Lege pro Woche ein Budget an (Name ist mit der aktuellen Kalenderwoche vorausgefüllt, aber änderbar). Trage Ausgaben ein – der Balken füllt sich und die Farbe wechselt automatisch:
  - unter 50 % → rosa
  - 50–75 % → violett
  - 75–100 % → rot
  - über 100 % → ein weinender Dino erscheint
- **Ziele**: Erstelle "Spardinos" mit Namen und Sparziel. Trage Beiträge ein – der Dino wird passend zum Fortschritt immer weiter ausgemalt.

Alle Daten werden lokal im Browser gespeichert (`localStorage`) – es gibt keinen Server und keine Anmeldung.

## Lokal ausprobieren

Einfach `index.html` doppelklicken bzw. im Browser öffnen.

## Auf GitHub veröffentlichen (GitHub Pages)

1. Erstelle ein neues Repository auf [github.com/new](https://github.com/new), z. B. `spardino`.
2. Lade `index.html` (und diese `README.md`) in das Repository hoch – entweder per Web-Oberfläche ("Add file → Upload files") oder per Git:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Erste Version von Spardino"
   git branch -M main
   git remote add origin https://github.com/DEIN-NUTZERNAME/spardino.git
   git push -u origin main
   ```
3. Gehe im Repository auf **Settings → Pages**.
4. Wähle bei "Branch" den Branch `main` und Ordner `/ (root)`, dann **Save**.
5. Nach kurzer Zeit ist die App unter `https://DEIN-NUTZERNAME.github.io/spardino/` erreichbar.

## Datei-Struktur

```
spardino/
├── index.html          ← die komplette App (HTML, CSS, JS)
├── images/
│   ├── dino-color.png     ← der fertig ausgemalte Dino
│   └── dino-outline.png   ← der "leere" Dino (Umriss)
└── README.md
```

Wichtig: Der Ordner `images/` muss beim Hochladen auf GitHub mit übertragen werden (nicht nur `index.html`), sonst fehlt dem Dino sein Bild.

## Den Dino austauschen

Willst du ein anderes Dino-Bild verwenden, ersetze einfach die beiden Dateien in `images/` durch deine eigenen (gleicher Dateiname, am besten mit transparentem Hintergrund und im Hochformat). Die App zeigt automatisch:
- `dino-outline.png` als "leeren" Zustand
- `dino-color.png` wird von unten nach oben passend zum Fortschritt eingeblendet

Farben, Texte und das Layout findest du direkt im `<style>`- bzw. `<script>`-Block von `index.html`.
