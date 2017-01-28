## Vorbereitung

### Tools installieren

Für diesen Teil des Tutorials brauchst du folgende Tools:

* Einen Code Editor
* GIT
* Ein Github Account

Wie man diese Sachen installiert wir im Kapitel [Django Girls Tutorial Installation](https://tutorial.djangogirls.org/en/installation/#install-a-code-editor) erklärt. Du musst nur die entsprechende Abschnitte beachten:

* Install  a code editor
* Install GIT
* Create a GitHub account

### Ein djangogirls ordner auf dein Rechner

Als nächstes brauchst du auf deinen Rechner ein Ordner wo du deine Codefiles dieses Workshops ablegen kannst. In den meisten fälle ist dein Home Directory eine gute Qahl. Auf Windows sieht dies zum beispiel so aus:`C:\Users\Name\` \(mit `Name` dein Login Name\).

> TIP: Auf Windows solltest du darauf achten das dieses Verzeichnis keine Spezialzeichen enthaltet. Wenn dein Benutzername Spezialzeichen enthaltet ist es besser ein andere Ordner zu wählen zum beispiel`C:\djangogirls`.

In dieses Verzeichnis machen wir jetzt ein neuer Ordner mit der Name `djangogirls`.

! Erstes mal command line: Hier sollten wir wohl noch mehr info einfügen \(was ist es wo ist es etc.\). nk: Ev. im Kapitel 'Tools' erklären.

command-line

```
$ mkdir djangogirls
$ cd djangogirls
```

Schliesse das Terminal noch nicht, du brauchst es nachher noch!

### Ein Repository auf Github

Wir wissen schon das Github ein Lagerplatz für Versionierte Code Projekte. Jedes Projekt hat sein eigenes sogenantes Repository. Das ist ein spezieller Ordner der eben auch die verschiedene Versionen und Änderungen für seine Files speichert. Die Magie hinter einem Repository steckt in einem unsichtbaren Unterordner der immer .git heisst. Wir werden also ein neues Repository auf Github machen und dieses dann auf unseren Rechner klonen.

Gehe im Browser zu `https://github.com/new` \(wenn du ein 404 Error bekommst musst du dich zuerst noch einloggen\). Nur das Feld Repository muss ausgefüllt werden und zwar mit_ _`username.github.io` wobei username dein Github Benutzername ist. Achte darauf das der Teil vor dem ersten Punkt genau mit deinen Github Benutzernamen übereinstimmt. Dies muss so sein weil Github nur Files in dieses Repository wie eine Webseite darstellt auf `http://username.github.io`.  Dann wähle Create Repository.

Jetzt kannst du wieder zurück zum Terminal gehen und das gerade gemachte repository zu deinen Rechner klonen mit untenstehendem Befehl. Ersetze dabei immer _username_ mit dein Github Benutzernamen, und ersetze _Your Name_ und _you@example.com_ durch deinen Namen und deine Emailaddresse. Die Zeilen ohne Dollar Zeichen '$' sollst du nicht eintippen. Dein Terminal sollte ungefähr das Antworten auf dem Befehl der Zeile vorher.

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

