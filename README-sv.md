<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Markdown 0.8.22

Textformatering för människor.

<p align="center"><img src="markdown-screenshot.png?raw=true" alt="Skärmdump"></p>

## Hur man formaterar text

Markdown är ett praktiskt sätt att redigera webbsidor. Skriv text som i ett e-postmeddelande och det blir en webbsida. Efter en kort stund händer det naturligt utan att du ens tänker på det. Här är [Markdown-syntaxen](http://commonmark.org/help/), en lista över [Markdown Extra funktioner](https://michelf.ca/projects/php-markdown/extra/) och [GitHub Flavored Markdown](https://help.github.com/en/articles/basic-writing-and-formatting-syntax). Förutom Markdown finns det förkortningar. Du kan lägga till [bilder](https://github.com/annaesvensson/yellow-image/tree/main/README-sv.md), [bildgallerier](https://github.com/annaesvensson/yellow-gallery/tree/main/README-sv.md), [videor](https://github.com/annaesvensson/yellow-youtube/tree/main/README-sv.md), [innehållsförteckningar](https://github.com/annaesvensson/yellow-toc/tree/main/README-sv.md), [ikoner](https://github.com/annaesvensson/yellow-fontawesome/tree/main/README-sv.md) och ytterligare funktioner på din webbplats.

## Exempel

Innehållsfil med namn på sidas och text:

    ---
    Title: Exempelsida
    ---
    Detta är ett exempelsida.

    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
    tempor incididunt ut labore et dolore magna pizza. Ut enim ad minim veniam, 
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo. 

Formatera text:

    Normal **fet** *kursiv* ~~struken~~ `code`

Skapa en lista:

    * objekt ett
    * objekt två
    * objekt tre

Skapa en sorterad lista:

    1. objekt ett
    2. objekt två
    3. objekt tre

Skapa en uppgiftslista:

    - [x] objekt ett
    - [ ] objekt två
    - [ ] objekt tre

Skapa en rubrik:

    # Rubrik 1
    ## Rubrik 2
    ### Rubrik 3

Skapa citat:

    > Citat
    >> Citat i citat
    >>> Citat i citat i citat

Skapa länkar:

    [Länk till sidan](/help/how-to-make-a-small-website)
    [Länk till fil](/media/downloads/yellow.pdf)
    [Länk till webbplats](https://datenstrom.se/sv/)

Lägga till bilder:

    [image photo.jpg Exempel]
    [image photo.jpg "Detta är en exempelbild"]
    [image photo.jpg "Detta är en särskilt lång beskrivning"]

Skapa tabeller:

    | Kaffe      | Mjölk | Styrka  |
    |------------|-------|---------|
    | Espresso   | nej   | stark   |
    | Macchiato  | ja    | medium  |
    | Cappuccino | ja    | svag    |

Skapa fotnoter:

    Text med en fotnot[^1] och några fler fotnoter.[^2] [^3]
    
    [^1]: Här är den första fotnoten
    [^2]: Här är den andra fotnoten
    [^3]: Här är den tredje fotnoten

Visa källkod:

    ```
    Källkoden visas oförändrad.
    function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    ```

Skapa paragraf:

    Här är första paragrafen. Text kan sträcka sig över flera rader
    och kan separeras med en tom rad från nästa paragrafen.

    Här är andra paragrafen. 

Skapa radbrytningar:

    Här är första raden⋅⋅
    Här är andra raden⋅⋅
    Här är tredje raden⋅⋅
    
    Mellanslag i slutet av raden representeras av prickar (⋅)

Skapa indikationer:

    ! Här är en indikation med varning 
    
    !! Här är en indikation med fel
    
    !!! Här är en indikation med tip

Använd CSS:

    ! {.class}
    ! Här är en indikation med anpassad klass.
    ! Text kan sträcka sig över flera rader
    ! och innehåller Markdown-textformatering.

Använd HTML:

    <strong>Text med HTML</strong> kan valfritt användas.
    <img src="/media/images/photo.jpg" alt="This is an example image">
    <a href="https://datenstrom.se" target="_blank">Öppna länken i en ny flik</a>.

Använd förkortningar:

    [image photo.jpg]     = lägga till en bild
    [gallery photo.*jpg]  = lägga till ett bildgalleri med popup
    [slider photo.*jpg]   = lägga till ett bildgalleri med reglaget
    [youtube fhs55HEl-Gc] = bädda in en video
    [toc]                 = göra ett innehållsförteckning

    Förkortningar kräver ytterligare tillägg för att fungera.

## Inställningar

Standardparsern definieras i filen `system/extensions/yellow-system.ini`. En annan parser kan definieras i [sidinställningarna](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md#inställningar-page) högst upp på varje sida, till exempel `Parser: markdown`. 

## Installation

[Ladda ner tillägg](https://github.com/annaesvensson/yellow-markdown/archive/main.zip) och kopiera zip-fil till din `system/extensions` mapp. Högerklicka om du använder Safari.

Detta tilläg använder [Markdown Extra 1.9.0](https://github.com/michelf/php-markdown) av Michel Fortin.

## Utvecklare

Datenstrom. [Få hjälp](https://datenstrom.se/sv/yellow/help/).
