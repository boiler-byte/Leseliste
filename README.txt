LESELISTE – INSTALLIERBARE PWA
==============================

Inhalt:
  index.html                Die Leseliste-App (Version 8, als PWA)
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

NEU IN VERSION 7
- Sortiergriff halten und bewegen: Die echte Comic-Karte folgt der Maus bzw.
  dem Finger direkt. Eine Markierung zeigt die Einfügeposition an.
- Funktioniert mit Touch, Stift und Maus; der Griff kann weiterhin per
  Pfeiltasten für eine barriereärmere manuelle Sortierung genutzt werden.
- Automatisches Scrollen beim Ziehen in die Nähe des Bildschirmrands.
- Optionale Notiz (maximal 220 Zeichen), direkt im Bearbeiten-Dialog.
- Notizen erscheinen auf der Karte; in der Mini-Ansicht auf zwei Zeilen
  begrenzt, die vollständige Notiz bleibt im Bearbeiten-Dialog erhalten.
- Notizen werden in IndexedDB und JSON-Backups gespeichert. Bestehende
  Datenbanken und bisherige JSON-Backups bleiben kompatibel.
- Offline-Cache für Version 7 aktualisiert.

NEU IN VERSION 8
- Dritte Darstellungsoption unter Menü -> Ansicht: Micro-Ansicht.
- Auf Tablets im Hochformat (ab 680 px) genau fünf Karten nebeneinander.
- Cover bildet weiterhin den gesamten Kartenhintergrund.
- Einzeiliger Titel, kleine Metadaten, kompakte Seitenzahl und Story-Status.
- Notiz wird bei Platzmangel auf eine Zeile gekürzt, bleibt beim Bearbeiten vollständig.
- Auf Smartphones je nach Breite zwei bis drei Karten nebeneinander.
- Ansichtswahl bleibt in IndexedDB gespeichert, bisherige Einträge kompatibel.
- Offline-Cache für Version 8 aktualisiert.
