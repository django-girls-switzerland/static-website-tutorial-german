## Vorbereitung

### Tools installieren

Für dieses Teil des Tutorials brauchst du folgende Tools:

* Ein code editor
* GIT
* Ein github account

Wie man diese sachen installiert ist erklärt im [Django Girls Tutorial Installation](https://tutorial.djangogirls.org/en/installation/#install-a-code-editor) Kapitel. Du musst nur die entsprechende Abschnitte beachten:

* Install  a code editor
* Install GIT
* Create a GitHub account

### Ein djangogirls ordner auf dein Rechner

Als nächstes brauchst du auf deinen Rechner ein Ordner wo du deine codefiles dieses Workshops ablegen kannst. In den meisten fälle ist dein Home Directory eine gute wahl. Auf Windows sieht dies zum beispiel so aus:`C:\Users\Name\` \(mit `Name` dein Login Name\).

> TIP: Auf Windows solltest du darauf achten das dieses Verzeichnis keine Spezialzeichen enthaltet. Wenn dein Benutzername Spezialzeichen enthaltet ist es besser ein andere Ordner zu wählen zum beispiel`C:\djangogirls`.

In dieses Verzeichnis machen wir jetzt ein neuer Ordner mit der Name `djangogirls`.

! Erstes mal command line: Hier sollten wir wohl noch mehr info einfügen \(was ist es wo ist es etc.\).

command-line

```
$ mkdir djangogirls
$ cd djangogirls
```

Schliesse das Terminal noch nicht, du brauchst es nachher noch!

### Ein Repository auf Github

Wir wissen schon das Github ein Lagerplatz für Versionierte Code Projekte. Jedes Projekt hat sein eigenes sogenantes Repository. Das ist ein spezieller Ordner der eben auch die verschiedene Versionen und Änderungen für seine Files speichert. Die Magic hiner ein Repository steckt in einen unsichtbaren Unterordner der immer .git heisst. Wir werden also ein neues repository auf github machen, und dies dann zu unserem Rechner 'clonen'.

Gehe im Browser zu `https://github.com/new` \(wenn du ein 404 Error bekommst musst du dich zuerst noch einloggen\). Nur das Feld Repository muss ausgefüllt werden und zwar mit_ _`username.github.io` wobei username dein Github Benutzername ist. Achte darauf das der Teil vor dem ersten Punkt genau mit deinen Github Benutzernamen übereinstimmt. Dies muss so sein weil Github nur Files in dieses Repository wie eine Webseite darstellt auf `http://username.github.io`.  Dann wähle Create Repository.

Jetzt kannst du wieder zurück zum Terminal gehen und das gerade gemachte repository zu deinen Rechner clonen mit folgenden Befehl \(ersetze immer _username_ mit dein Github Benutzernamen, und ersetze _Your Name_ und _you@example.com_ durch deinen Namen und deine Emailaddresse. Die Zeilen ohne  dollar zeichen sollst du nicht typen, dein Terminal sollte ungefähr das Antworten auf dem Befehl der Zeile vorher\):

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

Jetzt solltest du im djangogirls Ordner ein Ordner mit der namen `username.github.io` haben. Lasse das Terminal immer noch offen, du Brauchst es immer wieder um mit Git zu arbeiten und deine gemachte änderungen zu Github zu 'pushen'.

