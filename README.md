# Linux-Basiswissen

## System

### Den Rechner herunterfahren

`shutdown` oder `poweroff`, ggf. `sudo` nötig

### Benutzungshilfen

* Mit Tabulator kann man die aktuelle Eingabe automatisch vervollständigen lassen.
So bekommt man z. B. Datei- und Ordnernamen vervollständigt oder auch Befehle.
* Pfeiltaste nach oben ruft die zuletzt verwendeten Befehle auf, mit Enter können diese dann ausgeführt werden.
* Mit Strg-C können obige Vorgänge (und auch die meisten Programme) abgebrochen werden.

### Dateisystem

#### Im Dateisystem navigieren


`ls -lha`

* `cd ..`
* `cd /`

#### Dateiberechtigungen

Berechtigung | Kürzel | Zahlenwert
--- | --- | ---
Lesen | r | 1
Schreiben | w | 2
Ausführen* | x | 4

*Bei Ordnern steht das Ausführungs-Bit für die Anzeige der Ordnerinhalte.

#### Textdateien

##### less

##### nano

## Anwendungen

### MySQL / MariaDB

#### Dumps
Dumpen:
mysqldump wikidb -u root -p > wikidb.sql

Einspielen:
mysql -u root -p wikidb < wikidb.sql

