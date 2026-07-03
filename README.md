# Rampenruf App

Kostenloser MVP für Fahrer-Registrierung und Rampenzuweisung.

## Was funktioniert

- Smartphone-optimiert: große Buttons, responsive Admin-Kartenansicht und SMS-/Telefon-Links.
- Fahrer registrieren sich per QR-Code / Webformular.
- Admin sieht Warteliste.
- Admin trägt Rampe ein, z. B. 60.
- Admin kann einen SMS-Link öffnen. Das öffnet die SMS-App mit fertigem Text.
- Status: wartet, gerufen, erledigt.

## Wichtig

Echter automatischer SMS-Versand ist nicht dauerhaft kostenlos. Twilio/MessageBird/SMSAPI kosten Geld oder haben stark eingeschränkte Testkonten. Dieser MVP nutzt deshalb kostenlose SMS-Links: Ein Mitarbeiter klickt auf „SMS öffnen“ und sendet die Nachricht vom Handy.

## Kostenlos hosten

Empfohlen:

- GitHub Pages für die Web-App
- Supabase Free Plan für Datenbank

## Einrichtung

1. Supabase-Projekt erstellen.
2. In Supabase SQL Editor den Inhalt von `database.sql` ausführen.
3. `config.example.js` in `config.js` kopieren.
4. `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `ADMIN_PIN`, `SITE_URL` eintragen.
5. Dateien auf GitHub Pages, Netlify oder einen internen Webserver hochladen.
6. `admin.html` öffnen und QR-Code anzeigen.
7. QR-Code ausdrucken und im Wartebereich aufhängen.
8. Auf dem Smartphone `index.html` für Fahrer oder `admin.html` für Lager/Admin öffnen. Über den Browser kann die Seite auch zum Homescreen hinzugefügt werden.

## Datenschutz-Hinweis

Telefonnummern und Kennzeichen sind personenbezogene Daten. Für echten Betrieb brauchst du mindestens einen kurzen Datenschutzhinweis, klare Löschfristen und Zugriffsschutz.

## Nächste sinnvolle Erweiterungen

- echter Login für Admins
- automatische Löschung alter Einträge
- mehrere Standorte
- feste Rampenliste
- optional bezahlter SMS-Gateway
