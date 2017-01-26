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

## HTML: strukturieren

In die Einführung \(How the internet works\) haben wir schon mal über HTML geredet. HTML steht für HyperText Markup Language. HTML besteht aus sogenantent Tags. Es gibt 3 Typen von Tags:

* &lt;Elementname&gt; : Starttag
* &lt;/Elementname&gt; : Endtag
* &lt;Elementname/&gt; : Leertag

Das Starttag und Endtag werden immer zusammen verwendet. Der Tekst zwischen den beiden Tags ist das Element. Das Tag sagt etwas darüber aus wie der tekst zwischen den Start- und Endtags dargestellt werden sollte. In folgende Tabelle findest du ein paar Beispiele.

| Erklärung | HTML |
| :--- | :--- |
| ordinary paragraph text | `<p>text</p>` |
| your most important heading | `<h1>A heading</h1>` |
| a heading at the next level | `<h2>A sub-heading</h2>` |
| a heading at the next level | `<h3>A sub-sub-heading</h3>`... and so on, up to`<h6>` |
| emphasize your text | `<em>text</em>` |
| strongly emphasize your text | `<strong>text</strong>` |
| go to another line | `<br/>`\(you can't put anything inside br\) |
| create a link | `<a href="http://djangogirls.org/">link</a>` |
| make a list | `<ul><li>first item</li><li>second item</li></ul>` |
| define a section of the page | `<div></div>` |

Jede HTML-Seite hat zudem eine Basisstruktur, die immer gleich is. Das äusere Tag-Paar ist immer das &lt;html&gt;...&lt;/html&gt;. Dann gibt est zwei Teilen: Head and Body. In Body kommen die informationen die auf der eigentliche Seite dargestellt werden sollten. Das Head Teil ist dazu da um Meta-Informationen zu definieren. Zum Beispiel der Titel der Seite, welche CSS Files verwendet werden sollen für das Layout, Keywords für die Suchmachine etc.  
Die ganze basisstruktur sieht also so aus:

```
<html>
    <head>
        ...
    </head>
    <body>
        ...
    </body>
</html>
```

  Damit bist du jetzt in der Lage deine Webseite in index.html ein bisschen besser zu gestalten. Du könntest zum Beispiel einen Text mit Titel machen und unten dran eine Liste mit links zu den Seiten von den anderen in deine Gruppe. Der Inhalt ist momentan nicht das wichtigste, hauptsache du spielst ein bisschen mit den HTML Tags herum.

Wenn du, während deinen Text in index.html mit HTML-tags am schmucken bist, mal schauen möchtest wie es dan aussiehen würde, kannst du die Datei zwischendurch auch immer wieder mit deinen Browser öffnen. \(Vorher speichern nicht vergessen!\)

![](/assets/tutorial_screenshot.png)

Wenn du zufrieden bist mit der Inhalt und Struktur deiner Seite, ist es zeit sie wieder online zu bringen. Dazu gehen wir zurück zum Terminal, das im Idealfall immer noch offen ist.

command-line

```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
$ git add --all
$ git commit -m "adding html"
[master 9bfcf50] adding html
 1 file changed, 20 insertions(+), 2 deletions(-)
 rewrite index.html (100%)
$ git push -u origin master
```

Noch dein Github Username und  Passwort eingeben, und schon ist die neuste version deiner Webseite online! Woohoow!

## CSS: deine eigene Layout

Bis jetzt hast du deine Seite zwar strukturieren können mit Titel und listen und Paragrafen, schön sieht das ganze aber noch nicht aus. Das werden wir jetzt ändern, und dazu werden wir CSS verwenden.

CSS steht für Cascading Style Sheets und ist eine Sprache die benutzt wird um das Layout von HTML-Seiten zu beschreiben. Wir werden unserem CSS code in ein separates File schreiben. So kann man es einfacher austauschen wenn wir irgendwann mal der Look aber nicht der Inhalt unsere Seite ändern Wollen. Ein CSS file ist ein normales Textfile das auf .css endet, so weiss jede \(na ja, jede programmierer, und du jetzt auch\)das da eine Layoutbeschreibung drinn ist.

Zuerst machen wir also ein neues textfile im gleichen Verzeichniss wo schon index.html drin ist. Ich nenne meins zum Beispiel main.css, aber du kannst deins auch einen anderen Namen geben, solange der auf .css endet. Dieses file kannst du jetzt mit deinem Code Editor öffnen, und dein erster CSS-Code reinschreiben:

```
h1 {
    color: #426493;
}
```

Dieser Code ändert die Farbe des wichtigsten Headings h1. Nachdem wir die Änderungen im CSS-File gespeichert haben, müssen wir jetzt noch in unserem index.html File irgendwie mitteilen wo der Browser das Layout für diese Seite dann suchen soll. Dazu ergänzen wir im index.html das folgende:

```
<html>
    <head>
        <title> ... </title>
        <link rel="stylesheet" href="main.css">
    </head>
    ...
```

Wenn du jetzt nach dem Speichern das index.html File in deinen Browser öffnest, sollte das h1-Heading jetzt Blau sein, weil \#426493 der Code von ein ganz bestimmtes Blau ist. Willst den Tekst lieber in eine andere Farbe haben? Gebe dann mal in Google "colorpicker" ein, suche dir eine Farbe aus die dir gefällt und kopiere den mit \# anfängenden Code in deinen css File an Stelle von \#426493.

So, wir haben erfolgreich CSS an unsere Webseite hinzu gefügt. Gleich werden wir noch viel mehr damit machen, aber erst speichern wir diesen erfolgreichen Schritt schon mal ab in GIT und stellen das Resultat ins Netz auf Github.

command-line

```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)

    main.css

no changes added to commit (use "git add" and/or "git commit -a")
$ git add --all
$ git commit -m "a little bit of css"
[master a0850fb] a little bit of css
 2 files changed, 4 insertions(+)
 create mode 100644 main.css
$ git push -u origin master
```

Noch dein Github Username und  Passwort eingeben, und schon ist die neuste version deiner Webseite online! Woohoow!

Schauen wir uns dem Code dem wir schon in unserem CSS-File geschrieben haben jetzt mal genauer an. Es sieht ähnlich aus wie im unterstehenden Bild, ausser das wir eine andere Farbe und ein andere Selector benutzt haben. Kannst du erraten was das CSS aus dem Bild macht? \(Falls du es ausprobieren willst kannst du den Code einfach unter den schön bestehenden Code in dein CSS-file schreiben, speichern und dir deine Webseite wieder im Browser anschauen. Da \#333333 ein sehr dunkles Grau ist, und damit schwierig von schwarz zu unterscheiden kannst du dem am besten durch eine andere Farbe ersetzen.\)![](/assets/cssrule.png)Bild von [https://www.girldevelopit.com/materials](https://www.girldevelopit.com/materials) unter Creative Commons

Das was wir geschreiben haben nennt sich ein CSS-Rule. Um das ganze Layout von eine Webseite zu beschreiben benutzt man viele von diesen CSS-Regeln. Man kann sie einfach untereinander im CSS file schreiben. Ein Regel kann mehrere Deklarationen enthalten. Deklarationen sind dabei immer von der Form `Eigenschaft: Wert;` .

Wir können zum beispiel unseren css-Regel mit selector h1 wie folgt erweiteren:

```
h1 {
    background-color: #426493;
    color: #ffffff;
}
```

Wir können zum beispiel auch die Schriftarten ändern:

```
body{
    font-family: "Courier New", Courier, monospace;
}    
h1 {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #426493;
    color: #ffffff;
}
```

Andere beispiele von Schriftarten kannst du bei w3schools finden: [http://www.w3schools.com/cssref/css\\_websafe\\_fonts.asp](http://www.w3schools.com/cssref/css\_websafe\_fonts.asp) Diese Fonts werden oft benutzt und sind meistens ohne weiteres Vorhanden. Wenn du exotischere schriftarten benutzen möchtest ist es gut auch die Schriftart selber zu verfügung zu stellen, da diese nicht automatisch schon vom Browser gekannt ist. Mehr info dazu findest du im Kapitel [/extras-zu-deine-statische-webseite.md](/extras-zu-deine-statische-webseite.md)

Bis jetzt haben wir immer der Namen des HTML-Tags als CSS Selector benutzt. Das ist sinnvoll wenn der CSS-Regel sich auf alle Headings, Paragraphen oder Links bezieht. Was aber wenn nur ein spezifisches Element oder eine Gruppe von Elemente eine bestimmte Layout brauchen? Für dem Fall brauchen wir eine andere Art von Selectoren: Klassen und IDs. Jedes HTML-Tag kann man eine Class und eine id mitgeben. Dabei darf jede id aber nur einmal pro HTML-Seite vorkommen. Zu eine Class dagegen dürfen mehrere Elemente gleichzeitig gehören.

| Name | Benutzung im HTML-File | Benutzung im CSS-File |
| :--- | :--- | :--- |
| ID | `<p id="one_green_thing"> some green text </p>` | `#one_green_thing{ color: #00ff00;}` |
| Class | `<h1 class="all_red_things">Red title</h1> <p class="all_red_things"> some red text </p>` | `.all_red_things{ color: #ff0000;}` |

Die  `<span>` und `<div>` HTML-Tags sind beide generische Container, wobei span ein inline Element ist, und der Textflow also nicht unterbricht, und div ein Block Element. Diese beiden Elemente werden oft in Kombination mit Klassen oder IDs verwendet um Bestimmte teilen einer Seite ein bestimmtes Layout zu geben. Das kann dan zum beispiel so aussehen.

index.html

```
<html>
    <head>
        <title>Django Girls Bern</title>
        <link rel="stylesheet" href="main.css">
    </head>
    <body>
        <div id="header">
            <h1>Was ist Django Girls Bern</h1>
        </div>
        <div id="content">
            <p>Django Girls Bern ist ein Workshop wo man Programmieren lernt. </p>
            <p>Während zwei Tage machen wir eine eigene <span class="color">Webseite</span>, 
            mit einen <span class="color">Blog</span>. 
            Dazu verwenden wir verschiedene Tools, Frameworks und Programmiersprachen. Ein paar Beispiele sind:</p>
            <ul>
                <li><a href="https://de.wikipedia.org/wiki/Hypertext_Markup_Language">HTML</a></li>
                <li><a href="https://de.wikipedia.org/wiki/Cascading_Style_Sheets">CSS</a></li>
                <li><a href="https://de.wikipedia.org/wiki/Git">GIT</a></li>
                <li><a href="https://de.wikipedia.org/wiki/Python_(Programmiersprache)">Python</a></li>
                <li><a href="https://de.wikipedia.org/wiki/Django_(Framework)"><span id="big_django">Django</span></a></li>
                <li><a href="https://de.wikipedia.org/wiki/Kommandozeile">Command line</a></li>
            </ul>
            <p>Alle sind super motiviert und die Coaches haben viel geduld. Zudem gibt es feines Essen.</p>
        </div>
    </body>
</html>
```

main.css

```
body{
    margin: 0;
    padding: 0;
    font-family: "Courier New", Courier, monospace;
}

h1 {
    font-family: Arial, Helvetica, sans-serif;
    color: #ffffff;
}

#header {
    text-align: center;
    padding-top: 25px;
    padding-bottom: 25px;
    background-color: #426493;
}

#content {
    width: 75%;
    margin-top: 25px;
    margin-left: auto;
    margin-right: auto;
}

a {
    color: #426493;
}

.color{
    font-weight: bold;
    color: #426493;
}

#big_django{
    font-size: 200%;
    font-weight: bold;
}
```

Und das Resultat:  
![](/assets/statische-seite.jpg)

Ein Paar Beispiele von Sachen die man mit CSS machen kann kannst du dich von diesen Beispiel sicher abschauen. Für mehr Beispiele kannst du bei [w3schools](http://www.w3schools.com/css/default.asp) vorbei schauen. Probier ein paar Sachen aus, versuche aber nicht sofort die perfekt gestylte Webseite zu machen. Und zum Schluss bringen wir das ganze natürlich noch einmal online:

command-line

```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   index.html
	modified:   main.css

no changes added to commit (use "git add" and/or "git commit -a")
$ git add --all
$ git commit -m "a complete web page including css"
[master 80c1d78] a complete web page including css
 2 files changed, 63 insertions(+), 22 deletions(-)
 rewrite index.html (87%)
$ git push -u origin master
```



