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


### Git

#### Ändern, von welchem anderen Branch ein Branch abzweigt

`git rebase --onto neuer_wurzelbranch alter_wurzelbranch mein_branch`

Erklärung:
* Irgendwann waren wir mal auf `alter_wurzelbranch` (`git checkout alter_wurzelbranch`)
* Dort haben wir den neuen Branch `mein_branch` abgezweigt (`git checkout -b mein_branch`)
* Wir haben auf `mein_branch` etwas committet (`git commit`)
* Nun stellen wir fest, dass wir `mein_branch` besser von `neuer_wurzelbranch` abgezweigt hätten, z. B. weil dort schon etwas Code liegt, den wir in unserem Branch benötigen.
* Lösung: `git rebase --onto neuer_wurzelbranch alter_wurzelbranch mein_branch`
* Nun ist alles so, als wären wir zu Beginn auf `neuer_wurzelbranch` gewesen.


### MySQL / MariaDB

#### Dumps
Dumpen:
mysqldump wikidb -u root -p > wikidb.sql

Einspielen:
mysql -u root -p wikidb < wikidb.sql
