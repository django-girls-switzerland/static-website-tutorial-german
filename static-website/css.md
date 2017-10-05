## CSS: Deine eigenes Design

Bis jetzt hast du deine Seite zwar mit Titeln, Listen und Paragrafen strukturiert, so richtig schön sieht das ganze aber noch nicht aus. Das werden wir jetzt ändern und zwar mit CSS.

CSS steht für Cascading Style Sheets und ist eine Sprache die benutzt wird um das Design von HTML-Seiten zu beschreiben. Wir werden unseren CSS Code in ein separates File schreiben, so können wir das Design einfacher austauschen wenn wir irgendwann mal einen anderen Look für unsere Seite wollen. Eine CSS Datei ist ein normale Textdatei die auf .css endet, so wissen alle \(na ja, alle ProgrammiererInnen, und du jetzt auch\), dass da eine Designbeschreibung drin ist.

Zuerst machen wir also ein neues Textfile im gleichen Verzeichniss wo schon index.html drin ist. Ich nenne meins zum Beispiel `main.css`, aber du kannst deinem auch einen anderen Namen geben, solange er die Datei auf .css endet. Diese kannst du jetzt mit deinem Code Editor öffnen, und deinen ersten CSS-Code reinschreiben:

```
h1 {
    color: #426493;
}
```

Dieser Code ändert die Farbe des wichtigsten Headings 'h1'. Nachdem wir die Änderungen im CSS-File gespeichert haben, müssen wir jetzt noch unserem `index.html` File mitteilen wo der Browser das Layout für diese Seite suchen soll. Dazu ergänzen wir im `index.html` Folgendes:

```
<html>
    <head>
        <title> ... </title>
        <link rel="stylesheet" href="main.css">
    </head>
    ...
```

Wenn du dein CSS File nicht `main.css` genannt hast musst du den Dateinamen in der HTML-Datei \(nach `href="`\) entsprechend anpassen!

Wenn du nach dem Speichern das `index.html` File in deinem Browser öffnest, sollte das h1-Heading jetzt Blau sein. Denn `\#426493` ist der Farbcode von einem ganz bestimmten Blau. Willst den Text lieber in einer anderen Farbe haben? Dann gebe mal in Google "colorpicker" ein, suche dir eine Farbe aus die dir gefällt und kopiere die Nummer mit dem '\#' in deine CSS-Datei an Stelle von `\#426493`.

So, wir haben erfolgreich CSS zu unserer Webseite hinzu gefügt. Gleich werden wir noch viel mehr damit machen, aber erst speichern wir diesen erfolgreichen Schritt schon mal in Git und stellen so das Resultat ins Netz. D.h. wir 'deployen' die Änderungen an unserer Webseite.

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
$ git push
```

Noch dein GitHub Username und Passwort eingeben, und schon ist die neuste Version deiner Webseite online! Woohoo!

Schauen wir uns dem Code dem wir schon in unsere CSS-Datei geschrieben haben jetzt mal genauer an. Es sieht ähnlich aus wie im unterstehenden Bild, ausser das wir eine andere Farbe und einen anderen Selektor benutzt haben. Kannst du erraten was das CSS aus dem Bild macht? \(Falls du es ausprobieren willst kannst du den Code einfach unter den schon bestehenden Code in deine CSS-Datei schreiben, speichern und dir deine Webseite wieder im Browser anschauen. Da `\#333333` ein sehr dunkles Grau, und schwierig von schwarz zu unterscheiden ist, ersetzt du es am besten durch eine andere Farbe.\)
![](/assets/cssrule.png)Bild von [https://www.girldevelopit.com/materials](https://www.girldevelopit.com/materials)

Was wir in unsere CSS-Datei geschreiben haben nennt sich CSS-Regeln. Um das ganze Design einer Webseite zu beschreiben braucht es ganz viele von diesen CSS-Regeln. Man kann sie einfach untereinander in eine CSS-Datei schreiben. Eine Regel kann dabei mehrere Deklarationen enthalten. Deklarationen sind immer in der Form `Eigenschaft: Wert;`.

Wir können zum Beispiel unsere CSS-Regel mit dem Selector 'h1' wie folgt erweitern:

```
h1 {
    background-color: #426493;
    color: #ffffff;
}
```

Und zusätzlich ändern wir noch die Schriftarten:

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

Beispiele von anderen Schriftarten kannst du bei w3schools finden: [http://www.w3schools.com/cssref/css\\_websafe\\_fonts.asp](http://www.w3schools.com/cssref/css_websafe_fonts.asp) Diese Schriftarten werden oft benutzt und  funktionieren meistens ohne Weiteres. Wenn du exotischere Schriftarten benutzen möchtest ist es gut die Schriftart selber zu Verfügung zu stellen, da der Browser sie nicht automatisch kennt. Mehr Info dazu findest du hier: [MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts)

Bis jetzt haben wir immer der Namen des HTML-Tags als CSS-Selektor benutzt. Das ist sinnvoll wenn die CSS-Regel sich auf alle Titel, Paragraphen oder Links bezieht. Was aber wenn nur ein spezifisches Element oder eine Gruppe von Elementen ein bestimmtes Design brauchen? Für diesen Fall brauchen wir eine andere Art von Selektoren: Klassen und IDs. Jedem HTML-Tag kann man eine oder mehrere Klassen und eine ID mitgeben. Dabei darf jede ID aber nur einmal pro HTML-Seite vorkommen. Zu einer Klasse dagegen dürfen mehrere Elemente gleichzeitig gehören.

| Name | Benutzung im HTML-File | Benutzung im CSS-File |
| :--- | :--- | :--- |
| ID | `<p id="one_green_thing"> some green text </p>` | `#one_green_thing{ color: #00ff00;}` |
| Class | `<h1 class="all_red_things">Red title</h1> <p class="all_red_things"> some red text </p>` | `.all_red_things{ color: #ff0000;}` |

Die  `<span>` und `<div>` HTML-Tags sind beide generische Container, wobei `<span>` ein inline Element d.h. es unterbricht den Textflow nicht. `<div>` ist ein Block Element. Diese beiden Elemente werden oft in Kombination mit Klassen oder IDs verwendet um bestimmten Teilen einer Seite ein bestimmtes Design zu geben. Das kann dann zum Beispiel so aussehen.

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
            <p>Während zwei Tagen machen wir eine eigene <span class="color">Webseite</span>, 
            mit einem <span class="color">Blog</span>. 
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

Ein paar Beispiele von Sachen die man mit CSS machen kann kannst du dir von davon Beispiel abschauen. Weitere Beispiele findest du auf [w3schools](http://www.w3schools.com/css/default.asp). Probier ein paar Sachen aus, versuche aber nicht sofort die perfekt gestylte Webseite zu machen.

Zum Schluss bringen wir das Ganze natürlich noch einmal online:

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
$ git push
```

Gratuliere, du hast es geschafft! Du hast den zweiten Teil dieses Workshops beendet und hast deine eigene Webseite auf GitHub veröffentlicht. Geh mal schauen wie es aussieht und sei stolz auf dich!

Wenn du dein Erfolg gebührend gefeiert hast kannst du zurück zur [Übersicht](../README.md) gehen und mit Teil 3 'Einführung in Python' weitermachen.



