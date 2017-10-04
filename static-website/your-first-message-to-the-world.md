## Deine erste Mitteilung an die Welt

Im `username.github.io` Ordner erstellen wir eine Datei die `index.html` heisst. Da eine leere Datei nicht so interessant ist öffnen wir die Datei direkt mit dem Code Editor (Atom) und schreiben etwas rein. Was du genau schreibst spielt keine Rolle. Falls dir nichts einfällt schreibe 'Einhörner machen mich glücklich :)'. Nachdem die Datei gespeichert ist gehen wir wieder zur Kommandozeile um die Datei ins Internet zu bringen.

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

Git hat also die `index.html` Datei gesehen aber noch nicht gespeichert. Damit Git deine Änderungen festhält muss man zusätzlich zum Speichern im Code Editor, die Daten auch in Git speichern. Das Speichern in Git heisst 'commit'. Es erstellt eine Version von deinen Projekt \(alle Dateien im `username.github.io` Ordner in diesem Fall\) die du jederzeit wiederherstellen kannst. Zum Commit gehört immer eine Commit-Message. Dies ist eine kurze Beschreibung deiner Änderungen seit dem letzten Commit. Das Committen in Git geht so:

command-line

```
$ git add --all
$ git commit -m "first commit: just saying something"
[master (root-commit) 4eca6ab] first commit: just saying something
 1 file changed, 2 insertions(+)
 create mode 100644 index.html
```

Jetzt braucht es nur noch einen kleinen Schritt um unsere Webseite online zu bringen. Wir müssen unsere Änderungen zu Github hochladen. Das macht man mit dem 'push' Kommando:

command-line

```
$ git push -u origin master
```

Du musst dein Github Username und Passwort eingeben, dann wird dein Commit an GitHub geschickt. Du hast jetzt eine (sehr minimalistische) Webseite publiziert! Gehe im Brower zu 'http://username.github.io' ('username' durch deinen eigenen Username ersetzen!), da solltest du solltest du den Text sehen den du in `index.html` geschrieben hast.

Hattest du in index.html einen Text über mehrere Zeilen geschrieben? Wie sieht er im Browser aus? Falls dein Text nur eine Zeile lang war kannst du jetzt noch versuchen einen Text über mehrere Zeilen zu schreiben und den ganzen Commit-Prozess zu wiederhohlen. Du wirst sehen, dass der Browser keine Zeilenumbrüche erkennt. Deswegen werden wir HTML benutzen, damit können wir den Text auf unsere Seite so strukturieren wie wir wollen. Genau das werden wir im nächsten Teil machen. Aber zuerst hast du eine Pause verdient. ☕️



