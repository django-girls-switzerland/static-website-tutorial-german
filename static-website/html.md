## HTML: strukturieren

In die Einführung \(How the internet works\) haben wir schonmal über HTML geredet. HTML steht für Hyper Text Markup Language und besteht aus sogenannten 'HMTL-Tags'. Es gibt 3 Typen von diesen Tags:

* &lt;Elementname&gt; : Start-Tag
* &lt;/Elementname&gt; : End-Tag
* &lt;Elementname/&gt; : Leer-Tag

Start-Tags und End-Tags werden immer zusammen verwendet. Der Text zwischen den beiden Tags ist das Element. Das Tag sagt etwas darüber aus, wie der Text zwischen Start- und End-Tag dargestellt werden soll. Manche Tags brauchen keinen Text, in diesem Fall benutzt man ein Leer-Tag. Ein Leer-Tag ist wie ein Start- und ein End-Tag kombiniert, ohne Text zwischen den beiden. In der folgenden Tabelle findest du ein paar Beispiele.

| Erklärung | HTML |
| :--- | :--- |
| ordinary paragraph text | `<p>text</p>` |
| your most important heading | `<h1>A heading</h1>` |
| a heading at the next level | `<h2>A sub-heading</h2>` |
| a heading at the next level | `<h3>A sub-sub-heading</h3>`... and so on, up to`<h6>` |
| emphasize your text | `<em>text</em>` |
| strongly emphasize your text | `<strong>text</strong>` |
| go to another line | `<br/>`\(you can't put anything inside br, it's a 'Leertag'\) |
| create a link | `<a href="http://djangogirls.org/">link text</a>` |
| make a list | `<ul><li>first item</li><li>second item</li></ul>` |
| define a section of the page | `<div></div>` |

[Hier](https://www.w3schools.com/TAgs/ref_byfunc.asp) findest du eine Liste mit allen HTML-Tags und ihrer Bedeutung.

In einer HTML-Datei werden verschiedene HTML-Tags zur Strukturierung des Inhaltes verwendet. Tags können dabei verschachtelt werden. Wenn zum Beispiel ein Titel ein Link enthält sieht dies so aus:

```
<h1>Titel mit <a href="http://something.com">Link</a></h1>
```

Jede HTML-Datei hat zudem die gleiche Basisstruktur. Das äusserste Tag-Paar ist immer das `<html>...</html>`. Dann gibt es zwei Teile: 'Head' und 'Body'. In den 'Body' kommen die Informationen die auf der Seite dargestellt werden, die Inhalte. Der 'Head' Teil ist dazu da Meta-Informationen zu definieren. Zum Beispiel der Titel der Seite, CSS-Files für das Design, Keywords für die Suchmachine etc.

Die Basisstruktur sieht also immer so aus:

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

Damit die HTML-Datei nicht nur für den Browser, sondern auch für normale Menschen ein bisschen lesbarer ist, rückt man verschachtelte Tags mittels Leerzeichen ein.

Damit kannst du jetzt deine Webseite in der Datei `index.html` schreiben. Du kannst zum Beispiel einen Titel machen und darunter eine Liste mit Links zu den Seiten deiner Django Girls-Kolleginnen. Der Inhalt ist momentan nicht so wichtig, Hauptsache du spielst ein bisschen mit den HTML-Tags herum.

Wenn du zwischendurch schauen möchtest wie deine Webseite aussiehen würde, kannst du die Datei immer wieder mit dem Browser öffnen. \(Speichern nicht vergessen!\)

![](/assets/tutorial_screenshot.png)

Wenn du zufrieden bist mit dem Inhalt und der Struktur deiner Seite, ist es Zeit sie wieder online zu bringen, d.h. sie zu 'deployen'. Dazu gehen wir zurück in die Kommandozeile, die im Idealfall immer noch offen ist.

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
$ git push
```

Deinen GitHub-Username und -Passwort eingeben und schon ist die neuste Version deiner Webseite online! Woohoo :D!

Jetzt weisst du (fast) alles über HTML, was es zu wissen gibt. Kannst du uns noch einen Gefallen tun und ein Bild von einem Einhorn in deine Webseite einbauen? Eine Katze wäre auch okay, wenn dir das lieber ist. Findest du heraus, was für einen HTML-Tag du dazu brauchst und wie es funktioniert?

Wenn du das Bild vom Einhorn (oder der Katze) auf deiner Webseite eingebunden hast kannst du mit dem nächsten [Kapitel](./css.md) weitermachen und deine Webseite richtig schön stylen.

