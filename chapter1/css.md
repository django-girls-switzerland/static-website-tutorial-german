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



