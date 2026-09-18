# AlltagWahr

Behalte wiederkehrende Ausgaben – Abos, Versicherungen, Miete, Mitgliedschaften – im Blick. Als installierbare Web-App (PWA) fürs iPhone, komplett lokal, ohne Server, ohne Tracking.

## Funktionen

- Monatliche Gesamtbelastung + Jahreshochrechnung
- Kategorien-Übersicht als Donut-Chart (eigenes SVG, keine externe Bibliothek)
- „Kündigungs-Radar": warnt rechtzeitig vor auslaufenden Kündigungsfristen
- Einträge mit einem Tipp als „bezahlt" markieren → nächste Fälligkeit wird automatisch gesetzt
- Backup als JSON exportieren/importieren
- Optionale lokale Erinnerungen (Browser-Benachrichtigung beim Öffnen der App)
- Hell-/Dunkelmodus (Start immer im Hellmodus)
- Offline nutzbar dank Service Worker
- Alle Daten bleiben ausschließlich auf dem Gerät (`localStorage`) – keine Cloud, kein Backend, kein Tracking, keine externen Schriftarten/Skripte

## Struktur

```
index.html        App-Oberfläche
style.css          Design (Neumorphismus, Systemschriften)
app.js             Gesamte App-Logik
manifest.json       PWA-Manifest
sw.js               Service Worker (Offline-Cache)
icon-192.png, icon-512.png, apple-touch-icon.png, maskable-icon-512.png   App-Icons
impressum.html       Impressum (Angaben ausfüllen!)
datenschutz.html     Datenschutzerklärung
LICENSE              MIT-Lizenz für den eigenen Code
```

## Veröffentlichung über GitHub Pages (kostenlos)

1. Neues Repository auf GitHub anlegen (z. B. `alltagwahr`).
2. Diesen Ordnerinhalt in das Repository hochladen (z. B. per Drag & Drop im Browser oder `git push`).
3. Im Repository unter **Settings → Pages** als Quelle den Branch `main` und Ordner `/ (root)` auswählen.
4. Nach kurzer Zeit ist die App unter `https://DEIN-BENUTZERNAME.github.io/alltagwahr/` erreichbar.

## Installation auf dem iPhone

1. Die GitHub-Pages-URL in **Safari** öffnen (wichtig: Safari, nicht Chrome – nur Safari kann PWAs auf dem iPhone installieren).
2. Auf das Teilen-Symbol tippen.
3. **„Zum Home-Bildschirm"** wählen.
4. Die App erscheint danach wie eine normale App auf dem Homescreen, startet im Standalone-Modus (ohne Browserleiste) und funktioniert auch offline.

## Vor dem Veröffentlichen unbedingt erledigen

- **`impressum.html`**: die markierten Platzhalter durch echten Namen, Anschrift und E-Mail-Adresse ersetzen. Ohne echte Angaben ist das Impressum nicht rechtsgültig.
- Optional: Namen im Footer von `LICENSE` anpassen.

## Wichtiger Hinweis zu den Erinnerungen

Echte, vom Betriebssystem im Hintergrund zugestellte Push-Benachrichtigungen (auch wenn die App geschlossen ist) benötigen technisch einen Server, der die Push-Nachricht zum richtigen Zeitpunkt auslöst – das ist mit einer kostenlosen, rein statischen GitHub-Pages-Seite nicht umsetzbar. Die in dieser App eingebaute Erinnerungsfunktion zeigt Hinweise deshalb **beim Öffnen der App** an, wenn eine Zahlung oder Kündigungsfrist ansteht, nicht als Hintergrund-Push.

## Lizenz

Der eigene Code steht unter der MIT-Lizenz (siehe `LICENSE`). Es werden keine externen Bibliotheken oder Schriftarten eingebunden – keine zusätzlichen Lizenzbedingungen Dritter zu beachten.
