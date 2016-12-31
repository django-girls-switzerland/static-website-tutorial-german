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

Jetzt kannst du wieder zurück zum Terminal gehen und das gerade gemachte repository zu deinen Rechner clonen mit folgenden Befehl \(ersetze immer username mit dein Github Benutzernamen\):

command-line

```
$ git clone https://github.com/username/username.github.io
$ cd username.github.io
```

Jetzt solltest du im djangogirls Ordner ein Ordner mit der namen username.github.io haben. Lasse das Terminal immer noch offen, du Brauchst es immer wieder um mit Git zu arbeiten und deine gemachte änderungen zu Github zu 'pushen'. 

## Deine erste Mitteilung an die Welt

ein normaler text schreiben und pushen

## HTML: strukturieren

verschiedene HTML tags benutzen

## CSS: deine eigene Layout

CSS file zufügen

CSS schreiben

