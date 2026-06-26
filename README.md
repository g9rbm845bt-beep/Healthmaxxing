# Healthmaxxing — Cut Tracker

Een kleine, zelfstandige web-app om een cut (en later een lean bulk) te volgen:
gewicht, calorieën en eiwit invoeren, met automatisch 7-daags gemiddelde, trend
(kg/week), geschat onderhoud en voortgang richting een doelgewicht.

**Live:** _volgt na GitHub Pages-deploy_

## Features
- Dagelijkse invoer: gewicht, kcal (met betrouwbaar j/n), eiwit, notities
- Automatisch 7-daags gewichtsgemiddelde + lineaire trend
- Geschat onderhoud en voortgangsbalk richting doelgewicht
- Grafiek van gewichtsverloop met 7-daagse lijn en doellijn
- Werkt offline (PWA) en is installeerbaar op telefoon en desktop
- JSON-backup / -import en CSV-export

## Privacy
De code bevat **geen persoonlijke data**. Alles wat je invoert blijft lokaal in je
browser (localStorage). Maak af en toe een JSON-backup via de knop onderaan.

## Lokaal draaien
Open `index.html` in je browser. Voor de PWA-functies (installeren/offline) moet de
app via `http(s)` geserveerd worden, bijvoorbeeld:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Tech
Pure HTML/CSS/JS, geen build-stap, geen dependencies. Eén `index.html` + een
service worker (`sw.js`) en `manifest.webmanifest` voor de PWA.
