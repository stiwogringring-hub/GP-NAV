# GP-NAV (ohne Dropdown für Streckennummer)

Dieses Repo enthält eine eigenständige HTML-Seite, in der die **Streckennummer** nicht mehr per Dropdown, sondern **frei per Eingabe** erfolgt. Die Karte basiert auf **Leaflet** (CDN) und die Streckendaten liegen als GeoJSON (`GJ`-Konstante) in der Seite.

## Live betreiben (GitHub Pages)
1. Repository auf GitHub anlegen und die Dateien aus diesem Ordner pushen.
2. In den Repo-Settings **Pages** aktivieren und als Source `Branch: main`, `Folder: /root` auswählen.
3. Nach dem Build ist die Seite unter `https://<dein-user>.github.io/<repo-name>/` erreichbar.

## Lokal öffnen
Da alles clientseitig ist, reicht es, die Datei `index.html` im Browser zu öffnen. Für saubere CORS-Bedingungen empfiehlt sich ein kleiner lokaler Webserver:

### Python 3
```bash
python -m http.server 8080
```
Dann im Browser: http://localhost:8080/

## Änderungen gegenüber der Originalversion
- `<select id="strecke"></select>` → `<input id="strecke" placeholder="z. B. 1020" inputmode="numeric" size="8" />`
- Entfernte JS-Logik, die das Dropdown aus den GeoJSON-Features befüllt hat.

## Ordnerstruktur
```
.
├─ index.html       # fertige App (Leaflet + GeoJSON, freie Streckeneingabe)
├─ README.md        # dieses Dokument
├─ LICENSE          # MIT-Lizenz
└─ .gitignore
```

## Lizenz
MIT – siehe `LICENSE`.
