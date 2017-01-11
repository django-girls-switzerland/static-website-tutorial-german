# Eine Statische Webseite

Der erste Tag vom Workshop hat gerade angefangen und du bist schon dran sachen im Internet zu publizieren, cool oder? Aber wozu dauert der workshop dann 2 Tage? Um das zu verstehen müssen wir der Unterschied zwischen statische und dynamische webseiten erklären. Wir werden nämlich während unserem Workshop beide machen, und sie dann kombinieren.

## Statische und Dynamische Webseiten

Ein statische Webseite ist eine seite die als ganzes auf dem Server liegt, und genau so angezeigt wird wie sie mal gemacht wurde. Es ist nicht möglich mit den Besucher der Webseite zu interagieren. Man kann natürlich schon Links in die Seite haben die auf andere Seiten zeigen, und die kann der Benutzer anklicken, worauf auch diese Seiten dan genau so angezeigt werden wie sie auf dem Server liegen. Es ist aber nicht möglich ein Formular das der Benutzer ausfüllt zu verarbeiten, oder Daten aus eine Datenbank an zu zeigen, das alles geht nur mit dynamische Seiten. Um eine Statische Seite zu machen braucht es die Programmiersprachen HTML \(für der Struktur\) und CSS \(für das Layout\).

Dynamische Seiten sind ein bisschen komplizierter als statische Seiten. Sie bestehen meistens aus sogenannten Templates, wo dann je nach Situation dynamische Daten eingefügt werden können bevor sie zum Benutzer geschickt werden. Templates benützen HTML und CSS  und sehen deswegen ähnlich aus wie statische Webseiten, mit einem Unterschied, sie haben nähmlich Lücken, wo die dynamische Daten reinkommen müssen. Um die Lücken zu füllen braucht es eine weitere Programmiersprache, in unserem Fall ist dies Python. Oft benutzen dynamische Webseiten zudem eine Datenbank, um informationen, so wie Blogposts, Kommentare von verschiedene Benutzer, Likes usw zu speichern. So ist es auf eine dynamische Webseite möglich das ein Benutzer ein Formular ausfüllt, und die Seite, dynamisch ein Antwort generiert.

![](/assets/statisch-dynamisch.jpg)

## Tools

Wir fangen also mit eine statische Webseite an, und werden also zuerst HTML und CSS lernen. Zusätzlich werden wir uns mit ein paar Programmiertools vertraut machen. Nämlich mit einen Code Editor \(das MS Word/ Libreoffice Writer für Programmierer\), und mit Git und Github.

Git ist ein Versionierungssystem. Vielleicht hast du schon mal erlebt das du zum beispiel einen Bericht schreiben möchtest und am ende zig Files auf dein computer hast mit Namen wie bericht\_v1, bericht\_v2\_korrektur, bericht\_final? Dieses Chaos bei deine Codefiles zu vermeiden ist der Job von Git. Git merkt sich deine Änderungen, so dass du die Files nicht mehr umbenennen musst, und trotzdem jederzeit zu eine alte Version zurückkehren kannst. Zudem kanst du zu jede Version ein kleiner Kommentar schreiben, der dir helft zu wissen was du wann geändert hast.

Github hat wie der Name schon verrät was mit Git zu tun. Es ist nämlich einen zentrales Lager im Internet wo du mit Hilfe von Git diene Codefiles ablegen kannst. Das Ziel von Github ist es das du von überal auf deine Codefiles zugreifen kannst. Zudem kann man auf Github gut zusammen an einen Porgrammierprojekt arbeiten indem mehrere Leute die files auf Github abändern. Da viele Softwareprojekte zu gross sind um alleine zu machen und die Teams oft nicht im gleichen Raum sondern über die ganze Welt verteilt arbeiten ist Github ein sehr beliebtes Tool bei Software Entwicklern.

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

> NOTE: Auf Windows solltest du darauf achten das dieses Verzeichnis keine Spezialzeichen enthaltet. Wenn dein Benutzername Spezialzeichen enthaltet ist es besser ein andere Ordner zu wählen zum beispiel`C:\djangogirls`.

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

Du musst dein Github Username und Passwort eingeben, dann wird dein commit an github übergeben. Du hast jetzt eine sehr minimalistische webseite publiziert! Wenn du im browser zu [http://username.github.io](http://\_username\_.github.io) gehst solltest du den Text sehen den du in index.html geschrieben hast.

Hattest du in index.html einen text über mehrere Zeilen geschrieben? Wie sieht er aus im Browser? Falls dein text nur eine Zeile lang war kannst du jetzt noch versuchen einen text über mehrere Zeilen zu schreiben und das ganze Commit-prozess zu wiederhohlen. Du wirst sehen das der Browser keine Zeilenumbrüche erkennt. Deswegen werden wir HTML benutzen müssen um den Text auf unsere Seite zu strukturieren. Genau das werden wir im nächsten Teil machen. Aber zuerst hast du eine Pause verdient.

## HTML: strukturieren

verschiedene HTML tags benutzen

## CSS: deine eigene Layout

CSS file zufügen

CSS schreiben

