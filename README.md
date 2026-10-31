# Stahlball

Arena-Ballspiel im Browser, Orks gegen Trolle. Eine einzige HTML-Datei ohne Build-Schritt, als App installierbar (PWA) und offline spielbar.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Das komplette Spiel (HTML, CSS, JavaScript) |
| `sw.js` | Service Worker: Offline-Betrieb und Updates |
| `manifest.webmanifest` | App-Name, Icons, Vollbild im Hochformat |
| `icons/` | App-Icons |
| `fonts/` | Schriften Teko und Barlow Semi Condensed, lokal ausgeliefert (SIL Open Font License) |
| `netlify.toml` | Sicherheits-Header und Caching |

## Erstmalig veröffentlichen

1. Auf GitHub ein neues Repository anlegen, zum Beispiel `stahlball` (privat reicht).
2. Den Inhalt dieses Ordners hochladen: im Repository „Add file“ → „Upload files“, alle Dateien und Ordner hineinziehen, committen.
3. In Netlify „Add new site“ → „Import an existing project“ → GitHub → Repository `stahlball` wählen.
4. Build command leer lassen, Publish directory `.` (steht schon in `netlify.toml`), „Deploy“.
5. Unter „Domain management“ einen sprechenden Namen setzen, zum Beispiel `stahlball.netlify.app`.

## Auf dem Handy installieren

- Android (Chrome): Seite öffnen, Menü → „App installieren“.
- iPhone (Safari): Teilen → „Zum Home-Bildschirm“.

Danach startet das Spiel im Vollbild und läuft auch ohne Netz.

## Änderungen ausrollen

1. Neue `index.html` ins Repository hochladen.
2. In `sw.js` die Zeile `const CACHE = 'stahlball-vX';` hochzählen und mit hochladen.
3. Netlify baut automatisch neu. Installierte Apps holen sich die neue Version beim nächsten Start mit Netz.

## Datenschutz

Keine Cookies, keine Analyse, keine externen Dienste. Die Schriften liegen im Repository, es werden also keine Google-Server angefragt. Gespeichert wird nur lokal im Browser: gewähltes Team, Schwierigkeit und Ton an/aus.
