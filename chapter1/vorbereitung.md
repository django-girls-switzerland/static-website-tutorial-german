## Vorbereitung

### Tools installieren

Für diesen Teil des Tutorials brauchst du folgende Tools:

* Einen Code Editor
* GIT
* Ein Github Account

Wie man diese Sachen installiert wird im Kapitel [Django Girls Tutorial Installation](https://tutorial.djangogirls.org/en/installation/#install-a-code-editor) erklärt. Du musst nur folgende Abschnitte beachten:

* Install  a code editor
* Install GIT
* Create a GitHub account

### Ein djangogirls Ordner auf deinem Rechner

Als nächstes brauchst du auf deinen Rechner ein Ordner wo du deine Codefiles dieses Workshops ablegen kannst. In den meisten Fällen ist dein Home Directory eine gute Wahl. Auf Windows sieht dies zum Beispiel so aus:`C:\Users\Name\` \(mit `Name` dein Login Name\).

> TIP: Auf Windows solltest du darauf achten das dieses Verzeichnis keine Spezialzeichen enthält. Wenn dein Benutzername Spezialzeichen enthält ist es besser einen anderen Ordner zu wählen zum beispiel`C:\djangogirls`.

In diesem Verzeichnis erstellen wir jetzt einen neuen Ordner mit dem Namen `djangogirls`.

Dazu müssen wir das Terminal öffnen \(Mehr zum Terminal kannst du im Abschnitt [Tools](/chapter1/tools.md) lesen\)

Wir schreiben hier wo du das Terminal am Wahrscheinlichsten finden kannst. Dein Coach hilft dir gern weiter wenn du es Trotzdem nicht findest:

Für Windows:

Go to Start menu → All Programs → Accessories → Command Prompt.

Für OS X:

Go to Applications → Utilities → Terminal.

Für Linux:

Go to Applications → Accessories → Terminal

Bevor du die folgende Befehle eingibst sollst du zusammen mit dein Coach sicherstellen das du dich im Terminal am richtigen Ort befindest!

command-line

```
$ mkdir djangogirls
$ cd djangogirls
```

Schliesse das Terminal noch nicht, du brauchst es nachher noch!

### Ein Repository auf Github

Wir wissen schon das Github ein Lagerplatz für versionierte Code Projekte. Jedes Projekt hat sein eigenes sogenantes Repository. Das ist ein spezieller Ordner der eben auch die verschiedene Versionen und Änderungen für seine Files speichert. Diese Magie hinter einem Repository steckt in einem unsichtbaren Unterordner der .git heisst. Wir werden also ein neues Repository auf Github machen und dieses dann auf unseren Rechner klonen. Dadurch wird es auch in unserem Filesystem auftachen. 

Gehe im Browser zu `https://github.com/new` \(wenn du einen 404 Error bekommst musst du dich zuerst noch einloggen\). Nur das Feld Repository muss ausgefüllt werden und zwar mit_ _`username.github.io` wobei username dein Github Benutzername ist. Achte darauf das der Teil vor dem ersten Punkt genau mit deinen Github Benutzernamen übereinstimmt. Dies muss so sein weil Github nur Files in diesem Repository wie eine Webseite darstellt auf `http://username.github.io`. Dann wähle Create Repository.

Jetzt kannst du wieder zurück zum Terminal gehen und das gerade gemachte Repository mit dem untenstehende Befehl auf deinen Rechner klonen. Ersetze dabei immer _username_ mit dein Github Benutzernamen, und ersetze _Your Name_ und _you@example.com_ durch deinen Namen und deine Emailaddresse. Die Zeilen ohne Dollar Zeichen '$' sollst du nicht eintippen, da sind die Antworten des Computers auf deine Befehle. Dein Terminal sollte ungefähr so antworten wie im Beispiel unten.

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

Jetzt solltest du im djangogirls Ordner ein Ordner mit dem Namen `username.github.io` haben. Lasse das Terminal immer noch offen, du brauchst es immer wieder um mit Git zu arbeiten und deine Änderungen zu Github zu 'pushen'.

