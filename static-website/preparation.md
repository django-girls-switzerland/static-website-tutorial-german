## Letzte Vorbereitungen
Das sind die letzten Vorbereitungen bevor wir endlich zu den spannenden Teilen des Workshops kommen und unsere eigene Webseite bauen.

### Ein djangogirls Ordner auf deinem Laptop erstellen

Als erstes brauchst du auf deinen Laptop einen Ordner wo du die Code-Dateien dieses Workshops ablegen kannst. In den meisten Fällen ist dein Home Directory eine gute Wahl. Auf Windows sieht dies zum Beispiel so aus:`C:\Users\Name\` \(mit `Name` deinem Login Namen\).

> TIPP: Auf Windows solltest du darauf achten das der Ordnername keine Spezialzeichen enthält. Wenn dein Benutzername Spezialzeichen enthält ist es besser direkt einen anderen Ordner zu wählen zum Beispiel `C:\djangogirls`.

In diesem Ordner erstellen wir jetzt einen neuen Ordner mit dem Namen `djangogirls`.

Dazu müssen wir die Kommandozeile öffnen. Falls du nicht mehr weisst wie du das machst:

Für Windows:

Go to Start menu → All Programs → Accessories → Command Prompt.

Für OS X:

Go to Applications → Utilities → Terminal.

Für Linux:

Go to Applications → Accessories → Terminal

Bevor du die folgende Befehle eingibst sollst du zusammen mit deinem Coach sicherstellen das du dich in der Kommandozeile am richtigen Ort befindest!

command-line

```
$ mkdir djangogirls
$ cd djangogirls
```

Schliesse die Kommandozeile noch nicht, du brauchst sie später wieder!

### Ein Repository auf Github

Wir wissen schon das Github ein Lagerplatz für versionierte Code Projekte. Jedes Projekt hat sein eigenes sogenantes Repository. Das ist ein spezieller Ordner der eben auch die verschiedene Versionen und Änderungen für seine Files speichert. Die Magie hinter einem Repository steckt in einem unsichtbaren Ordner der .git heisst.
Nun werden wir ein neues Repository auf Github machen und dieses dann auf unseren Rechner duplizieren (klonen). Dadurch wird es auch in unserem Filesystem erscheinen. 

Gehe im Browser zu `https://github.com/new` \(falls du einen 404 Error bekommst musst du dich zuerst noch einloggen\). Das Feld 'Repository' muss mit `username.github.io` ausgefüllt werden wobei username dein Benutzername auf GitHub ist. Achte darauf das der Teil vor dem ersten Punkt genau mit deinen Github Benutzernamen übereinstimmt. Dies muss so sein weil GitHub nur Files in diesem Repository unter `http://username.github.io` als eine Webseite veröffentlicht. Danach klicke auf 'Create Repository'.

Jetzt kannst du wieder zurück zur Kommandozeile gehen und das gerade gemachte Repository mit dem untenstehende Befehl auf deinen Rechner duplizieren (klonen). Ersetze dabei immer _username_ mit deinem GitHub Benutzernamen, _Your Name_ durch deinen Namen und _you@example.com_ durch deine Emailaddresse.

Die Zeilen ohne Dollar Zeichen '$' sollst du nicht eintippen, das sind die Antworten des Computers auf deine Befehle!
Deine Kommandozeile sollte ungefähr so antworten wie im Beispiel unten.

command-line

```
$ git config --global user.name "Your Name"
$ git config --global user.email you@example.com
$ git clone https://github.com/username/username.github.io
Cloning into 'username.github.io'...
warning: You appear to have cloned an empty repository.
Checking connectivity... done.
$ cd username.github.io
```

Jetzt solltest du in deinem 'djangogirls' Ordner einen Ordner mit dem Namen `username.github.io` sehen. Lasse die Kommandozeile weiterhin offen, du brauchst es immer wieder um mit Git zu arbeiten und deine Änderungen zu Github zu spielen (zu 'pushen').

