<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Markdown 0.8.24

Text formatting for humans.

<p align="center"><img src="markdown-screenshot.png?raw=true" alt="Screenshot"></p>

## How to format text

Markdown is a practical way to edit web pages. Write text like you would in an email and it becomes a web page. After a short while, it happens naturally without you even thinking about it. Here's the [Markdown syntax](http://commonmark.org/help/), a list of [Markdown Extra features](https://michelf.ca/projects/php-markdown/extra/) and [GitHub Flavored Markdown](https://help.github.com/en/articles/basic-writing-and-formatting-syntax).

## How to customise text

There are shortcuts to add additional features. You can add [images](https://github.com/annaesvensson/yellow-image), [image galleries](https://github.com/annaesvensson/yellow-gallery), [icons](https://github.com/annaesvensson/yellow-icon) and additional features to your content. The available shortcuts depend on extensions installed.

The default content parser is defined in file `system/extensions/yellow-system.ini`. A different content parser can be defined in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of each page, for example `Parser: markdown`.

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

Making quotes:

    > Quote
    >> Quote of a quote
    >>> Quote of a quote of a quote

Making links:

    [Link to page](/help/how-to-make-a-small-website)
    [Link to file](/media/downloads/yellow.pdf)
    [Link to website](https://datenstrom.se)

Adding images:

    [image photo.jpg Example]
    [image photo.jpg "This is an example image"]
    [image photo.jpg "This is an especially long description"]

Making tables:

    | Coffee     | Milk | Strength |
    |------------|------|----------|
    | Espresso   | no   | strong   |
    | Macchiato  | yes  | medium   |
    | Cappuccino | yes  | weak     |

Making footnotes:

    Text with a footnote[^1] and some more footnotes.[^2] [^3]
    
    [^1]: Here's the first footnote
    [^2]: Here's the second footnote
    [^3]: Here's the third footnote

Showing source code:

    ```
    Source code will be shown unchanged.
    function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    ```

Making paragraphs:

    Here's the first paragraph. Text can span over several lines
    and can be separated by a blank line from the next paragraph.

    Here's the second paragraph.

Making line breaks:

    Here's the first line⋅⋅
    Here's the second line⋅⋅
    Here's the third line⋅⋅
    
    Spaces at the end of the line are shown with dots (⋅)

Making notices:

    ! Here's a notice with warning
    
    !! Here's a notice with error
    
    !!! Here's a notice with tip

Using CSS:

    ! {.class}
    ! Here's a notice with custom class.
    ! Text can span over several lines
    ! and contain Markdown text formatting.

Using HTML:

    <strong>Text with HTML</strong> can be used optionally.
    <img src="/media/images/photo.jpg" alt="This is an example image">
    <a href="https://datenstrom.se" target="_blank">Open link in new tab</a>.

Using shortcuts:

    [image photo.jpg]    = adding an image
    [gallery photo.*jpg] = adding an image gallery with popup
    [slider photo.*jpg]  = adding an image gallery with slider

Extension for custom shortcut:

```
<?php
class YellowExample {
    const VERSION = "0.1.2";
    public $yellow;         // access to API
    
    // Handle initialisation
    public function onLoad($yellow) {
        $this->yellow = $yellow;
    }
    
    // Handle page content of shortcut
    public function onParseContentShortcut($page, $name, $text, $type) {
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

## Acknowledgments

This extension includes [Markdown Extra 1.9.0](https://github.com/michelf/php-markdown) by Michel Fortin. Thank you for the good work.

## Installation

[Download extension](https://github.com/annaesvensson/yellow-markdown/archive/main.zip) and copy ZIP file into your `system/extensions` folder. [Learn more about extensions](https://github.com/annaesvensson/yellow-update).

## Developer

Anna Svensson. [Get help](https://datenstrom.se/yellow/help/).
