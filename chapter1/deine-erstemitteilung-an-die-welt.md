## Deine erste Mitteilung an die Welt

Im `username.github.io` Ordner erstellen wir jetzt eine Datei die `index.html` heist. Da eine leere Datei nicht so interessant ist öffnen wir jetzt die Datei mit den code editor den du vorher installiert hast und schreiben etwas rein. Nachdem die Datei gespeichert ist gehen wir wieder zum Terminal um die Datei ins internet zu bringen.

command-line

```
$ git status
On branch master
Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

    index.html

nothing added to commit but untracked files present (use "git add" to track)
```

Git hat also die `index.html` Datei gesehen aber noch nicht gespeichert. Damit git deine änderungen festhält muss man also zusätzlich zum speicheren in dem Code Editor, die Daten auch in git speichern. Das speichern in Git heist 'commit'. Es erstellt eine Version von deinen projekt \(alle Dateien im `username.github.io` Ordner in diesem Fall\) wozu du jederzeit zurückgehen kannst. Zum Commit gehört immer eine commit-message. Dies ist eine kurze Beschreibung von was du seit den letzten Commit geändert hast. Das committen in Git geht so:

command-line

```
$ git add --all
$ git commit -m "first commit: just saying something"
[master (root-commit) 4eca6ab] first commit: just saying something
 1 file changed, 2 insertions(+)
 create mode 100644 index.html
```

Jetzt braucht es nur noch einen schritt um unsere Webseite online zu bringen. Wir müssen nämlich unsere änderungen noch zu Github hochladen. Das macht man mit dem push command:

command-line

```
$ git push -u origin master
```

Du musst dein Github Username und Passwort eingeben, dann wird dein commit an github übergeben. Du hast jetzt eine sehr minimalistische webseite publiziert! Wenn du im browser zu [http://username.github.io](http://username.github.io) gehst solltest du den Text sehen den du in index.html geschrieben hast.

Hattest du in index.html einen text über mehrere Zeilen geschrieben? Wie sieht er aus im Browser? Falls dein text nur eine Zeile lang war kannst du jetzt noch versuchen einen text über mehrere Zeilen zu schreiben und das ganze Commit-prozess zu wiederhohlen. Du wirst sehen das der Browser keine Zeilenumbrüche erkennt. Deswegen werden wir HTML benutzen müssen um den Text auf unsere Seite zu strukturieren. Genau das werden wir im nächsten Teil machen. Aber zuerst hast du eine Pause verdient.

