LESELISTE – INSTALLIERBARE PWA
==============================

Inhalt:
  index.html                Die Leseliste-App (Version 4, als PWA)
  manifest.webmanifest      Installationsinformationen
  service-worker.js         Offline-Funktion
  icons/                    App-Icons

INSTALLATION
1. ZIP entpacken.
2. Den kompletten entpackten Ordner (mit allen Dateien) auf einem
   HTTPS-Webserver hochladen, z. B. GitHub Pages, Netlify oder
   deinen eigenen Webspace. Alternativ lokal über http://localhost
   starten (Beispiel: python -m http.server 8000 im App-Ordner).
3. Den Link im Browser aufrufen und die Seite einmal online laden.
4. Über Browser-Menü „App installieren“ bzw. „Zum Home-Bildschirm“
   die PWA installieren. Danach lässt sich die App offline öffnen.

WICHTIG ZU DEINEN DATEN
- Comic-Daten und Cover liegen weiterhin ausschließlich lokal in der
  IndexedDB des jeweiligen Browsers/der Website, nicht in der ZIP.
- Eine PWA unter HTTPS hat ggf. einen anderen Speicherbereich als die
  bisherige lokal geöffnete HTML-Datei oder eine andere Domain.
- Um alte Daten mitzunehmen: In der alten Leseliste über Menü → Export
  ein JSON-Backup erstellen; auf der gehosteten PWA Menü → Import nutzen.
- Regelmäßig über Menü → Export Sicherungen anlegen.
- Änderungen der Domain bzw. das Löschen von Website-Daten können
  den Zugriff auf lokal gespeicherte Comics verlieren lassen.

HINWEIS
Eine direkt per Doppelklick geöffnete index.html ist keine installierbare
PWA: Service Worker funktionieren nur über HTTPS oder localhost.

Die App benötigt keine externen Bibliotheken oder Netzwerkdienste.

NEU IN VERSION 4
- Kompakte Comic-Karten ohne Änderungsdatum und Zwischenüberschrift.
- Metadaten kurz als Vol, Pt und # angezeigt.
