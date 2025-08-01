## What HTML Tags are Allowed by Quickbase?

Quickbase allows for customization of the platform with HTML and CSS within certain features. JavaScript is supported within [code pages](https://helpv2.quickbase.com/hc/en-us/articles/4570389110036). Content is also constrained by limits such as character count as defined in our [limits page](https://helpv2.quickbase.com/hc/en-us/articles/4570306993940).

Quickbase may also block identified security vulnerabilities proactively and without notice to protect the security of the platform and our customers.

HTML and CSS is generally accepted within a few areas:

| AREA | SUPPORTED | UNSUPPORTED |
| --- | --- | --- |
| Code pages | 
-   Browser-supported HTML
-   Browser-supported CSS
-   Browser-supported JavaScript

 |   |
| Rich text fields, data entered by users (unsupported content may be accepted at entry but will not render for users) | “Display” HTML and CSS (to format and decorate text) as supported by the rendering browser and included in the identified list below | 

-   HTML or CSS that allows for interactivity such as, but not limited to:

-   Script tags
    
-   Event handlers
    
-   iFrames
    
-   Ajax calls
    

-   All JavaScript
-   Style tags

 |
| Text elements on a form, when HTML is turned on | 

-   bold
-   italics
-   paragraph
-   span
-   a
-   img
-   table
-   table row
-   table cell
-   table heading cell

 |   |
| Formula rich text fields, created by builders (unsupported content may be blocked during creation or runtime) | “Display” HTML and CSS (to format and decorate text) as supported by the rendering browser | 

-   HTML or CSS that allows for interactivity such as, but not limited to:

-   Script tags
    
-   Event handlers
    
-   iFrames
    
-   Ajax calls
    

-   All JavaScript
-   Style tags

 |
| 

Realm branding

-   Header
-   Footer
-   Sign-in page

 | Basic HTML used for display purposes | 

-   Script, object, embed, frameset, iframe, applet, html, body tags
-   JavaScript
-   CSS
-   Style tags

 |
| Email notifications | “Display” HTML and CSS (to format and decorate text) as supported by the rendering browser | 

-   HTML or CSS that allows for interactivity such as, but not limited to:

-   Script tags
    
-   Event handlers
    
-   iFrames
    
-   Ajax calls
    

-   All JavaScript
-   Style tags

 |
| Old Dashboards | “Display” HTML and CSS (to format and decorate text) as supported by the rendering browser and included in the identified list below | 

-   HTML or CSS that allows for interactivity such as, but not limited to:

-   Script tags
    
-   Event handlers
    
-   iFrames
    
-   Ajax calls
    

-   All JavaScript
-   Style tags

 |
| New Dashboards | Limited HTML for text decoration, using our editor |   |

## Tips and Tricks

### Inliner

Certain properties are not allowed to exist separately in a tag such as `style`, for security reasons. These properties may be include inline with HTML tags though. Tools such as the [Mailchimp Inliner](https://templates.mailchimp.com/resources/inline-css/) can help with this process.

### Quotes in a formula field

Within a formula field, quote marks `"` are used to define a text literal. Within a rich text field, the HTML is considered part of the text and must be defined with quotes. This will require quote marks to be escaped, as shown in our help article about [color-coding fields](https://helpv2.quickbase.com/hc/en-us/articles/4570255561108).

### Sample HTML Tags for use in supported areas

To learn more about these tags and see examples visit the [W3C site](http://www.w3schools.com/tags/default.asp).

| HTML TAGS FOR TEXT FIELDS |
| --- |
| a | for adding links |
| abbr | show tool tip for abbreviations |
| acronym | show tool tip for acronyms |
| address | show address |
| area | define area on an image map |
| article | defines an article with self contained content |
| aside | defines text to the side of other text |
| b | bold |
| bdi | bi-directional text |
| bdo | bi-directional override |
| big | bigger text |
| blockquote | indents a quotation or chunk of text |
| br | line break |
| br/ | line break |
| caption | caption text |
| cite | displays citations and references in italics |
| code | computer code |
| col | used to apply styling to an entire column in a table |
| colgroup | used to apply styling to a group of columns in a table |
| data | displays text associating it with a value key |
| dd | term description in definition list |
| del | indicates deleted text with a strikethrough |
| details | allows for a collapsible heading and details section |
| dfn | shows a definition term in italics |
| div | a section of a page |
| dl | definition list |
| dt | term in definition list |
| em | emphasized text (italics) |
| fieldset | outlines a group of fields, set of tags |
| figcaption | defines a caption for a photo |
| figure | used with figcaption |
| font | text format |
| footer | places a footer at the bottom of the page |
| h1 - h6 | headings of different sizes |
| header | used for headers |
| hr | horizontal rule |
| i | italics |
| img | image |
| ins | indicates inserted text with an underline |
| kbd | keyboard text |
| legend | caption for a fieldset |
| li | list item |
| map | image map |
| mark | used to highlight text |
| meter | defines a visual meter |
| nav | creates a list of navigation links |
| ol | ordered (numbered) list |
| p | paragraph |
| picture | more advanced ways to render images than img |
| pre | preformatted text |
| progress | generates a progress bar |
| q | quotation |
| s | creates strikethrough text |
| samp | sample computer code |
| section | creates sections in a page |
| small | smaller size text |
| source | an audio player |
| span | text span |
| strong | strong (bold) text |
| sub | subscript |
| summary | used with the details tag |
| sup | superscript |
| table, tbody, td, tfoot, th, thead, tr | creates a table with different properties |
| time | adds time keys to text |
| tt | teletype or mono spaced text |
| u | underline |
| ul | unordered (bulleted) list |
| var | variable |
| wbr | tells a browser where a word break is acceptable |