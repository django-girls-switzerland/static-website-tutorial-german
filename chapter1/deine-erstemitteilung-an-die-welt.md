## Deine erste Mitteilung an die Welt

Im `username.github.io` Ordner erstellen wir jetzt eine Datei die `index.html` heisst. Da eine leere Datei nicht so interessant ist öffnen wir jetzt die Datei mit dem Code Editor den du vorher installiert hast und schreiben etwas rein. Was du genau schreibst spielt nich so eine Rolle, du kannst einfach ein paar Wörter oder Sätze hineinschreiben die dir gerade einfallen. Nachdem die Datei gespeichert ist gehen wir wieder zum Terminal um die Datei ins internet zu bringen.

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

Git hat also die `index.html` Datei gesehen aber noch nicht gespeichert. Damit git deine Änderungen festhält muss man also zusätzlich zum speichern im Code Editor, die Daten auch in git speichern. Das speichern in Git heist 'commit'. Es erstellt eine Version von deinen Projekt \(alle Dateien im `username.github.io` Ordner in diesem Fall\) wohin du jederzeit zurückgehen kannst. Zum Commit gehört immer eine commit-message. Dies ist eine kurze Beschreibung von dem was du seit dem letzten Commit geändert hast. Das committen in Git geht so:

command-line

```
$ git add --all
$ git commit -m "first commit: just saying something"
[master (root-commit) 4eca6ab] first commit: just saying something
 1 file changed, 2 insertions(+)
 create mode 100644 index.html
```

Jetzt braucht es nur noch einen Schritt um unsere Webseite online zu bringen. Wir müssen unsere Änderungen noch zu Github hochladen. Das macht man mit dem push command:

command-line

```
$ git push -u origin master
```

Du musst dein Github Username und Passwort eingeben, dann wird dein commit an github übergeben. Du hast jetzt eine sehr minimalistische webseite publiziert! Wenn du im browser zu [http://username.github.io](http://username.github.io) gehst solltest du den Text sehen den du in index.html geschrieben hast.

Hattest du in index.html einen Text über mehrere Zeilen geschrieben? Wie sieht er aus im Browser? Falls dein Text nur eine Zeile lang war kannst du jetzt noch versuchen einen Text über mehrere Zeilen zu schreiben und den ganzen Commit-Prozess zu wiederhohlen. Du wirst sehen das der Browser keine Zeilenumbrüche erkennt. Deswegen werden wir HTML benutzen müssen um den Text auf unsere Seite zu strukturieren. Genau das werden wir im nächsten Teil machen. Aber zuerst hast du eine Pause verdient.



