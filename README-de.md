<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Markdown 0.9.4

Textformatierung für Menschen.

<p align="center"><img src="SCREENSHOT.png" alt="Bildschirmfoto"></p>

## Wie man eine Erweiterung installiert

[ZIP-Datei herunterladen](https://github.com/annaesvensson/yellow-markdown/archive/refs/heads/main.zip) und in dein `system/extensions`-Verzeichnis kopieren. [Weitere Informationen zu Erweiterungen](https://github.com/annaesvensson/yellow-update/tree/main/README-de.md).

## Wie man Text formatiert

Markdown ist eine praktische Art um Webseiten zu bearbeiten. Schreibe Text wie in einer E-Mail und daraus wird eine Webseite. Nach einer kurzen Zeit passiert das ganz natürlich, ohne dass man darüber nachdenkt. Das vorrangige Designziel der Markdown-Syntax besteht darin, sie so lesbar wie möglich zu machen. Hier sind die [Markdown-Syntax](http://commonmark.org/help/), [Markdown-Extra-Funktionen](https://michelf.ca/projects/php-markdown/extra/) und [GitHub-Flavored-Markdown](https://help.github.com/en/articles/basic-writing-and-formatting-syntax).

Der Standard-Inhaltsparser wird in der Datei `system/extensions/yellow-system.ini` festgelegt. Ein anderer Inhaltsparser lässt sich in den [Seiteneinstellungen](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md#einstellungen-seite) ganz oben auf jeder Seite festlegen, zum Beispiel `Parser: markdown`.

## Wie man Text mit Abkürzungen formatiert

Markdown ist eine schnelle Art um Webseiten zu bearbeiten. Markdown-formatierter Text kann mit jedem Texteditor geöffnet werden. Oder es kann im [Webbrowser](https://github.com/annaesvensson/yellow-edit/tree/main/README-de.md) bearbeitet werden. Die meisten Anwendungen unterstützen die grundlegende Markdown-Syntax, einige Anwendungen bieten Abkürzungen mit zusätzlichen Funktionen für Webseiten. Das gibt dir beispielsweise die Möglichkeit [Bilder](https://github.com/annaesvensson/yellow-image/tree/main/README-de.md) und [Bildergalerien](https://github.com/annaesvensson/yellow-gallery/tree/main/README-de.md) einzubinden. Abkürzungen sind praktisch für Leute die HTML und CSS nicht kennen. Die verfügbaren Abkürzungen hängen von den installierten Erweiterungen ab.

## Wie man Text mit Blockelementen formatiert

Markdown ist eine flexible Art um Webseiten zu bearbeiten. Setze das Zeichen `!` an den Zeilenanfang um ein allgemeines Blockelement zu erstellen. Das gibt dir beispielsweise die Möglichkeit einen ganzen Absatz in einer besonderen Farbe hervorzuheben. Als Webentwickler fragst du dich wahrscheinlich, kann ich damit `<div>...</div>` zu einer Webseite hinzufügen und wo warst du mein ganzes Leben lang? Die Antwort lautet ja und wie ein Diamant im Boden wartete er darauf gefunden zu werden. Blockelemente sind praktisch für Leute die HTML und CSS kennen. Die verfügbaren Blockelemente hängen vom deinem aktuellen Theme ab.

## Beispiele

Inhaltsdatei mit Seitentitel und Text:

    ---
    Title: Beispielseite
    ---
    Das ist eine Beispielseite.

    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
    tempor incididunt ut labore et dolore magna pizza. Ut enim ad minim veniam, 
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.

Text formatieren:

    Normal **Fettschrift** *Kursiv* ~~Durchgestrichen~~ `Code`

Eine Liste erstellen:

    * Punkt eins
    * Punkt zwei
    * Punkt drei

Eine sortierte Liste erstellen:

    1. Punkt eins
    2. Punkt zwei
    3. Punkt drei

Eine Aufgabenliste erstellen:

    - [x] Punkt eins
    - [ ] Punkt zwei
    - [ ] Punkt drei

Eine Überschrift erstellen:

    # Überschrift 1
    ## Überschrift 2
    ### Überschrift 3

Links erstellen:

    [Link zu Seite](/help/how-to-make-a-small-website)
    [Link zu Datei](/media/downloads/yellow-deutsch.pdf)
    [Link zu Webseite](https://datenstrom.se/de/)

Bilder hinzufügen:

    [image photo.jpg Beispiel]
    [image photo.jpg "Dies ist ein Beispielbild"]
    [image photo.jpg "Dies ist eine besonders lange Beschreibung"]

Tabellen erstellen:

    | Kaffee     | Milch | Stärke  |
    |------------|-------|---------|
    | Espresso   | nein  | stark   |
    | Macchiato  | ja    | mittel  |
    | Cappuccino | ja    | schwach |

Fußnoten erstellen:

    Text mit einer Fußnote[^1] und noch weiteren Fußnoten.[^2] [^3]
    
    [^1]: Hier ist die erste Fußnote
    [^2]: Hier ist die zweite Fußnote
    [^3]: Hier ist die dritte Fußnote

Quellcode anzeigen:

    ```
    Quellcode wird unverändert angezeigt.
    function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    ```

Absätze erstellen:

    Hier ist der erste Absatz. Der Text kann über mehrere Zeilen gehen
    und kann durch eine Leerzeile vom nächsten Absatz getrennt werden.

    Hier ist der zweite Absatz.

Zeilenumbrüche erstellen:

    Hier ist die erste Zeile⋅⋅
    Hier ist die zweite Zeile⋅⋅
    Hier ist die dritte Zeile⋅⋅
    
    Leerzeichen am Zeilenende sind dargestellt durch Punkte (⋅)

Zitate erstellen:

    > Zitat
    
    >> Zitat im Zitat
    
    >>> Zitat im Zitat im Zitat

Abkürzungen benutzen:

    [image photo.jpg] = Bild oder Miniaturbild hinzufügen
    [gallery photo]   = Bildergalerie mit Popup hinzufügen
    [slider photo]    = Bildergalerie mit Schieber hinzufügen

Blockelemente benutzen:

    ! Hier ist ein allgemeines Blockelement.
    ! Der Text kann über mehrere Zeilen gehen
    ! und Markdown-Textformatierung beinhalten.

    ! {.important}
    ! Hier sind Informationen die beachtet werden müssen.

    ! {.note}
    ! Hallo, dieser Text sieht aus wie ein Klebezettel.

CSS für eigenes Blockelement:

```
.content .example-block {
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: #f7f7f7;
    color: #333;
    border-radius: 12px;
}
```

Code für eigene Abkürzung:

```
<?php
class YellowExample {
    const VERSION = "0.1.3";
    public $yellow;         // access to API
    
    // Handle initialisation
    public function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    
    // Handle page content element
    public function onParseContentElement($page, $name, $text, $attributes, $type) {
        $output = null;
        if ($name=="example" && ($type=="block" || $type=="inline")) {
            $output = "<div class=\"".htmlspecialchars($name)."\">";
            $output .= "Add more HTML code here";
            $output .= "</div>";
        }
        return $output;
    }
}
```

## Danksagung

Diese Erweiterung enthält [Markdown Extra 1.9.0](https://github.com/michelf/php-markdown) von Michel Fortin. Danke für die gute Arbeit.

## Entwickler

Anna Svensson. [Hilfe finden](https://datenstrom.se/de/yellow/help/).
