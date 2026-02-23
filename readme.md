# Markdown 0.9.6

Text formatting for humans. Developed by Anna Svensson.

<p align="center"><img src="screenshot.png" alt="Screenshot" /></p>

## How to install an extension

[Download ZIP file](https://github.com/annaesvensson/yellow-markdown/archive/refs/heads/main.zip) and copy it into your `system/extensions` folder. [Learn more about extensions](https://github.com/annaesvensson/yellow-update).

## How to format text

Markdown is a practical way to edit web pages. Write text like you would in an email and it becomes a web page. After a short while, it happens naturally without you even thinking about it. The overriding design goal for the Markdown syntax is to make it as readable as possible. Here are the [Markdown syntax](http://commonmark.org/help/), [Markdown Extra features](https://michelf.ca/projects/php-markdown/extra/) and [GitHub Flavored Markdown](https://help.github.com/en/articles/basic-writing-and-formatting-syntax).

The default content parser is defined in file `system/extensions/yellow-system.ini`. A different content parser can be defined in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of each page, for example `Parser: markdown`.

## How to format text with shortcuts

Markdown is a quick way to edit web pages. Markdown-formatted text can be opened with any text editor. Or it can be edited in a [web browser](https://github.com/annaesvensson/yellow-edit). Most applications support the basic Markdown syntax, some applications provide shortcuts with additional features for web pages. This allows you, for example, to add [images](https://github.com/annaesvensson/yellow-image) and [image galleries](https://github.com/annaesvensson/yellow-gallery). Shortcuts are convenient for people who don't know HTML and CSS. The available shortcuts depend on extensions installed.

## How to format text with block elements

Markdown is a flexible way to edit web pages. Put the `!` character at the beginning of the line and you can make a general block element. This allows you, for example, to emphasise an entire paragraph in a special color or font. If you are a web developer you are probably asking, does this mean I can add `<div>...</div>` to a web page and where have you been all my life? The answer is yes and like a diamond in the ground it was waiting to be found. Colors, fonts, block elements and other CSS classes are defined in a theme. [Learn more about themes](https://datenstrom.se/yellow/help/how-to-customise-a-theme).

## Examples

Content file with page title and text:

    ---
    Title: Example page
    ---
    This is an example page.

    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
    tempor incididunt ut labore et dolore magna pizza. Ut enim ad minim veniam, 
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo. 

Formatting text:

    Normal **bold** *italic* ~~strikethrough~~ `code`

Making a list:

    * item one
    * item two
    * item three

Making an ordered list:

    1. item one
    2. item two
    3. item three

Making a task list:

    - [x] item one
    - [ ] item two
    - [ ] item three

Making a heading:

    # Heading 1
    ## Heading 2
    ### Heading 3

Making links:

    [Link to page](/help/how-to-make-a-small-website)
    [Link to file](/media/downloads/yellow-english.pdf)
    [Link to website](https://datenstrom.se)

Adding images:

    [image photo.jpg Example]
    [image photo.jpg "This is an example image"]
    [image photo.jpg "This is an especially long description"]

Making tables:

    | Coffee     | Milk | Strength |
    |------------|------|----------|
    | Espresso   | no   | strong   |
    | Cortado    | yes  | medium   |
    | Cappuccino | yes  | weak     |

Making footnotes:

    Text with a footnote[^1] and some more footnotes.[^2] [^3]
    
    [^1]: Here's the first footnote
    [^2]: Here's the second footnote
    [^3]: Here's the third footnote

Making paragraphs:

    Here's the first paragraph. Text can span over several lines
    and can be separated by a blank line from the next paragraph.

    Here's the second paragraph.

Making line breaks:

    Here's the first line⋅⋅
    Here's the second line⋅⋅
    Here's the third line⋅⋅
    
    Spaces at the end of the line are shown with dots (⋅)

Making quotes:

    > Quote
    
    >> Quote of a quote
    
    >>> Quote of a quote of a quote

Using shortcuts:

    [image photo.jpg] = adding an image or image thumbnail
    [gallery photo]   = adding an image gallery with popup
    [slider photo]    = adding an image gallery with slider

Using code blocks:

    ```
    Code will be shown unchanged.
    function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    ```

Using collapsible blocks:

    ? Show details
    ?
    ? This is a collapsible block element. It's  
    ? only shown when you click on the first line
    ? and can contain Markdown text formatting.

Using general blocks:

    ! Here's a general block element.
    ! Text can span over several lines
    ! and can contain Markdown text formatting.

    ! {.important}
    ! Here's information that needs attention.

    ! {.example}
    ! Here's a custom block element, can be customised with CSS.

CSS for custom block element:

```
.content .example {
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: #fffbf0;
    color: #333;
}
```

Extension file for custom shortcut:

```
<?php
// Example extension, https://github.com/annaesvenson/yellow-example

class YellowExample {
    const VERSION = "0.9.2";
    public $yellow;         // access to API
    
    // Handle initialisation
    public function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    
    // Handle page content element
    public function onParseContentElement($page, $name, $text, $attributes, $type) {
        $output = null;
        if ($name=="example" && ($type=="block" || $type=="inline")) {
            if (is_string_empty($text)) $text = "Hello World";
            $output = "<div class=\"example\">".htmlspecialchars($text)."</div>";
        }
        return $output;
    }
}
```

## Acknowledgements

This extension includes [Markdown Extra 1.9.1](https://github.com/michelf/php-markdown) by Michel Fortin. Thank you for the good work.

Do you have questions? [Get help](https://datenstrom.se/yellow/help/).
