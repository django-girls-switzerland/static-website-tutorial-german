# Deine statische Webseite zu Django einbinden

Wenn du das Django Girls Tutorial fertig durchgearbeitet hast möchtest du vielleicht deine statische Webseite vom ersten Tag in dein Django Projekt einbinden. zum Beispiel als 'About' Page für deinen Blog? Dieses Kapitel erklärt die wie du das machst.


## Die Dateien in dein Django Projekt verschieben

Der erste Schritt ist deine HTML- und CSS-Dateien an den Richtigen Ort in deinem Django Projekt zu verschieben. Das Bild unten zeigt dir, wie die Ordner und Files deines Django-Projektes im Moment angeordnet sind. 

> Achtung: Wenn du deine statische Webseite auf deiner github.io URL behalten willst solltest du die ursprünglichen Dateien da lassen wo sie waren, d.h. sie nur zu kopieren anstatt komplett zu verschieben.

![](/assets/django-blog-structure.jpg)

Dann fügst du alle deine HTML-Dateien dem Ordner `blog/templates/blog` hinzu und die CSS-Dateien dem Ordner `blog/static/css`. Das heisst du kopierst deine HTML-Dateien an den Ort wo schon die HTML-Dateien für dein Django-Projekt liegen und die CSS-Dateien an den Ort wo deine anderen CSS-Dateien liegen. Gleich zu gleich gesellt sich gern! :)

Für den Moment ist es sinnvoll wenn du deiner `index.html` Datei einen anderen, aussagekräftigeren Namen gibst, zum Beispiel `about.html`. Das Tutorial geht davon aus, dass du die Datei in `about.html` umbenannt hast und es über die URL '/about' anzeigen lassen willst. Wenn du einen anderen Dateinamen und eine andere URL vorziehst musst du entsprechend deine Dateinamen und deine URL verwenden für diese Anleitung.

## Die URL und eine einfache View hinzufügen

Lass uns jetzt deine statische Seite auf Django-Art verfügbar machen, dafür werden wir `urls.py` und `views.py` ergänzen.

Zuerst erstellen wir eine neue URL. Dazu fügen wir die neue URL (siehe Bild) den schon vorhandenen URLs hinzu im `urls.py` hinzu.

blog/urls.py

```
urlpatterns = [
    ...
    url(r'^about/$', views.about_page, name='about_page'),
]
```

Dann estellen wir eine neue, ganz einfach View, diese sollte so aussehen:

blog/views.py

```
def about_page(request):
    return render(request, 'blog/about.html', {})
```

Jetzt sollte deine statische Webseite auf `localhost:8000/about` erreichbar sein.

## Integration mit dem base.html Template

Okay nun haben wir unsere statische Webseite in unser Django-Projekt eingebunden und es ist über eine URL erreichbar. Aber die zwei Webseiten sehen noch völlig unterschiedlich aus, das ist nicht so schön. Hier ein paar Tipps wie du das Design der Projekte vereinheitlichen kannst:

Grundsätzlich ist es eine gute Idee Bootstrap weiterhin zu benutzen, so wie du es in deinem Django-Projekt gemacht hast. Bootstrap hilft dir dabei sehr schnell eine schöne Webseite zu bekommen. Wenn du mehr über Bootstrap erfahren möchtest schau dir am besten mal du die [offizielle Dokumentation](http://getbootstrap.com) an oder mache das [Tutorial auf Codecademy](https://www.codecademy.com/courses/web-beginner-en-yjvdd/0/1/) zu dem Thema.  

Füge folgende Tempate-Tags zu deiner `about.html` Datei hinzu:
* {% raw %} `{% extends 'blog/base.html' %}`_ {% endraw %}
* {% raw %} _`{% block content %}` {% endraw %}
* {% raw %} `{% endblock content %}` {% endraw %}

Der 'extends'-Tag sollte ganz zuoberst in deiner Datei stehen, der 'block'-Tag direkt darunter und der 'endblock'-Tag am Ende deiner Datei.

Jetzt kannst du noch die Teile deiner About-Seite entfernen die schon in der `base.html` Datei enthalten sind. Das sind folgende Tags:
* &lt;html&gt;
* &lt;head&gt;...&lt;/head&gt; (und alles dazwischen)
* &lt;body&gt; 
* Und alle anderen Inhalte wie Menüs die du nicht mehr möchtest.

Wenn du Teile des CSS von deiner statischen Seite wiederverwenden möchtest musst du diese entweder in die Datei `blog.css` einfügen oder Code-Linie aus about.html in der du auf deine CSS-Datei verlinkst in die Datei `base.html` rüberkopieren (zwischen die &lt;head&gt;...&lt;/head&gt; Tags).

Woohoo, nun hast du schon eine recht coole Webseite! Viel Spass damit :).





