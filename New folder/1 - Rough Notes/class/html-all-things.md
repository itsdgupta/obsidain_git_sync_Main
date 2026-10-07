# Html Notes
**By Divyansh Gupta**

## Introduction to HTML and CSS

### All Tags
- `<html>` : root element of the entire HTML document
    - `lang` : specifies the language of the page
- `<head>` : container for metadata and page information not displayed on the page
- `<meta>` : provides metadata about the document
    - `charset` : defines character encoding (value `UTF-8` supports almost all languages and special characters)
    - `name` : specifies the metadata name (value `viewport` makes the webpage responsive)
    - `content` : specifies value for the metadata name (value `width=device-width, initial-scale=1.0`)
- `<title>` : sets the title of the webpage for the browser tab and search engines
- `<body>` : contains all visible content of the webpage
- `<h1>` : defines a main heading
- `<p>` : defines a paragraph of text
- `<img>` : embeds an image
    - `src` : specifies the path to the image file
    - `alt` : provides alternate text for the image
    - `width` : defines the width of the element
- `<br>` : inserts a line break
- `<hr>` : creates a horizontal line
- `<input>` : creates a form input field
    - `type` : defines the input type (value `text`)
- `<link>` : links an external resource
    - `rel` : defines the relationship of the linked resource (value `stylesheet`)
    - `href` : defines the path or URL to the linked resource

### Definitions
- `HTML` : HyperText Markup Language, the standard markup language used to create and structure web content
- `HyperText` : text that contains links (hyperlinks) to other documents or resources
- `Markup` : use of special tags to define structure and meaning
- `CSS` : Cascading Style Sheets, the language used to style and design web pages
- `Cascading` : refers to the hierarchical order in which styles are applied
- `Style Sheets` : a collection of rules defining how HTML elements should be displayed
- `<!DOCTYPE html>` : Document Type Declaration used to tell the browser the document is HTML5
- `Tag` : a keyword enclosed in angle brackets that tells the browser how to structure or display content
- `Element` : the complete structure formed by an opening tag, content, and a closing tag
- `Attribute` : provides extra information about an HTML element using name-value pairs
- `Closing Tag` : marks the end of an HTML element using a forward slash
- `Self-Closing Tag` / `Void Element` : tags that do not contain content and do not require a closing tag

### Important Notes
- `<!DOCTYPE html>` must always be the very first line in the HTML file
- Without a closing tag, the browser may not display content correctly
- `UTF-8` character encoding is recommended as it supports almost all languages and special characters


<hr>

## Paragraph and Heading Tags

### All Tags
- `<p>` : defines a paragraph of text
    - `title` : tooltip text shown on hover
    - `lang` : language of the content
    - `dir` : text direction
        - `ltr` : left-to-right direction
        - `rtl` : right-to-left direction
    - `align` : (Deprecated) text alignment — use CSS instead
- `<h1>`–`<h6>` : defines hierarchical headings of different importance levels
    - `title` : same as `<p>`
    - `lang` : same as `<p>`
    - `dir` : same as `<p>`
    - `align` : same as `<p>`

### Definitions
- `block-level element` : an element that starts on a new line and takes the full available width
- `SEO` : search engine optimization; search engines give higher weight to content inside higher-level headings
- `deprecated` : indicates a feature is outdated and should be replaced by modern alternatives like CSS

### Important Notes
- do not put block-level elements (like headings, lists, or other paragraphs) inside a `<p>` tag
- closing the tag (e.g., `</p>`) is required in HTML5
- use headings in logical order and do not skip levels randomly
- there should normally be only one `<h1>` per page


<hr>

## HTML `<img>` Tag and Its Attributes

### All Tags
- `<img>` : used to embed images in a webpage
    - `src` : specifies the path or URL to the image file
    - `alt` : provides alternative text for accessibility or if the image fails to load
    - `width` : sets the display width of the image
    - `height` : sets the display height of the image
    - `loading` : specifies how the browser should load the image
        - `lazy` : delays loading until the image is near the viewport
        - `eager` : loads the image immediately
        - `auto` : lets the browser decide loading behavior based on heuristics
    - `title` : provides a tooltip that appears when the user hovers over the image
    - `srcset` : provides multiple image sources to match different screen resolutions or pixel ratios
    - `sizes` : specifies the intended display size of the image relative to the viewport
    - `usemap` : associates an image with an image map

### Definitions
- `self-closing tag` : a tag that does not require a separate closing tag
- `viewport` : the area of the webpage currently visible to the user
- `device pixel ratio` : the relationship between physical hardware pixels and logical CSS pixels
- `below the fold` : content that is not immediately visible on the screen upon initial page load
- `responsive images` : images that adapt to the display size and device resolution for better performance

### Important Notes
- the `loading` attribute defaults to `eager` if the browser does not support it
- use `lazy` for images below the fold to improve performance
- use `eager` for critical images like hero images that must load immediately


<hr>

## HTML Formatting, Quotation, and Citation Elements

### All Tags
- `<b>` : makes text bold without implying semantic importance
- `<i>` : italicizes text for emphasis or to denote special terms
- `<strong>` : indicates text with strong semantic importance
- `<em>` : indicates semantic emphasis for tone or stress
- `<mark>` : highlights text, typically with a yellow background
- `<small>` : denotes secondary information or fine print
- `<del>` : marks text as deleted with a strikethrough
- `<ins>` : marks text as newly inserted with an underline
- `<sub>` : formats text as subscript below the baseline
- `<sup>` : formats text as superscript above the baseline
- `<blockquote>` : defines a block-level section quoted from another source
    - `cite` : specifies the URL of the quotation source
- `<q>` : defines a short, inline quotation
    - `cite` : same as `<blockquote>`
- `<abbr>` : defines an abbreviation or acronym
    - `title` : specifies the full form or description shown on hover
- `<address>` : defines contact information for the document author or owner
    - `class` : a global attribute used to assign a CSS class
    - `id` : a global attribute used to assign a unique identifier
- `<cite>` : defines the title of a creative work
- `<bdo>` : overrides the default text direction
    - `dir` : specifies the text direction
        - `ltr` : left-to-right direction
        - `rtl` : right-to-left direction

### Definitions
- `global attributes` : attributes supported by most elements, such as `class` and `id`
- `Bi-Directional Override` : functionality to change the direction of text rendering

### Important Notes
- Use `<blockquote>` for long quotations; do not use it for short, inline quotes.
- Use `<q>` for short, inline quotations within a sentence.
- Use `<cite>` to identify the title of a creative work; do not use it for a person's name.
- `<blockquote>` and `<cite>` are distinct elements; `<blockquote>` contains the quote, while `<cite>` identifies the source or title.
- `<blockquote>` and `<cite>` are often used together to provide a quote followed by its attribution.


<hr>

## HTML Links

### All Tags
- `<a>` : defines a hyperlink for navigation
    - `href` : specifies the destination URL
    - `target` : specifies where the linked document opens
        - `_self` : opens the link in the same tab or window (default)
        - `_blank` : opens the link in a new tab or window
        - `_parent` : opens the link in the parent frame
        - `_top` : opens the link in the full body of the window
        - `Custom frame name` : opens the link in a specified frame with a matching name
    - `title` : provides additional information shown as a tooltip on hover
    - `download` : prompts the browser to download the linked resource
- `<frameset>` : container used to define frame layout
    - `cols` : defines the width of columns in the frameset
- `<frame>` : defines a specific frame within a frameset
    - `src` : specifies the URL of the document to load
- `<iframe>` : embeds another HTML document into the current page
    - `name` : assigns a name to the frame for targeting
    - `src` : same as `<frame>`
- `<body>` : contains the main content of the document
    - `id` : unique identifier used for bookmark navigation
- `<h1>` : defines a main heading
    - `id` : same as `<body>`
- `<h2>` : defines a sub-heading
    - `id` : same as `<body>`

### Definitions
- `Hyperlink` : a link created using an anchor tag to navigate between pages or sections
- `External Link` : a link that points to a different website or domain
- `Internal Link` : a link that points to another page or resource on the same website
- `Bookmark` : an internal link used to scroll to a specific section on the same page
- `Tooltip` : small descriptive text that appears when hovering over an element
- `Frameset` : a structure used to define layout areas where different documents can be displayed

### Important Notes
- The `target="_self"` attribute is the default behavior for links
- `<a>` tags require the `href` attribute for external or internal navigation
- Bookmarks require assigning an `id` to the target element and using `#` in the `href` attribute


<hr>

## HTML Tables

### All Tags
- `<table>` : defines the table
    - `border` : sets the border width in pixels
    - `align` : older attribute for alignment (prefer CSS)
    - `valign` : older attribute for vertical alignment (prefer CSS)
    - `width` : older attribute for width (prefer CSS)
- `<tr>` : defines a table row
- `<th>` : defines a table header cell
    - `colspan` : number of columns a cell should span
    - `rowspan` : number of rows a cell should span
    - `scope` : indicates whether the header applies to a row or column
        - `row` : header applies to the entire row
        - `col` : header applies to the entire column
        - `rowgroup` : header applies to the row group
        - `colgroup` : header applies to the column group
    - `id` : unique identifier for linking to headers
- `<td>` : defines a table data cell
    - `colspan` : same as `<th>`
    - `rowspan` : same as `<th>`
    - `headers` : links a data cell to one or more header cells using `id` values
- `<caption>` : defines a table caption
- `<thead>` : groups header content semantically
- `<tbody>` : groups body content semantically
- `<tfoot>` : groups footer content semantically

### Definitions
- `Tabular data` : data such as schedules, results, or comparisons organized in rows and columns
- `Accessibility` : features that ensure screen readers can correctly announce data with its proper heading
- `Semantic grouping` : using specific tags to define the structure (header, body, footer) of a table
- `Screen reader` : assistive technology used to read the table content aloud

### Important Notes
- `border`, `align`, `valign`, and `width` are older attributes; prefer CSS for styling in modern pages
- Always use `scope` or `headers` to provide context for screen readers, otherwise tables lack proper meaning
- Use `scope="col"` or `scope="row"` for most tables
- Use `headers` attribute specifically when tables are complex or one cell relates to multiple headers.


<hr>

## HTML Lists

### All Tags
- `<ul>` : defines an unordered list, typically displayed with bullet points
    - `type` : specifies the list marker style
        - `disc` : unordered list bullet style
        - `circle` : unordered list bullet style
        - `square` : unordered list bullet style
        - `1` : ordered numeric list style
        - `A` : ordered uppercase letter list style
        - `a` : ordered lowercase letter list style
        - `I` : ordered uppercase Roman numeral list style
        - `i` : ordered lowercase Roman numeral list style
- `<ol>` : defines an ordered list, typically displayed with numbers or letters
    - `type` : same as `<ul>`
    - `start` : specifies the starting number or letter of the list
    - `reversed` : reverses the order of the list
- `<li>` : defines a list item within `<ul>` or `<ol>`
    - `value` : sets a specific value for a list item
- `<dl>` : defines a description list for terms and their descriptions
- `<dt>` : defines a term in a description list
- `<dd>` : defines a description for a term in a description list

### Definitions
- `unordered list` : list format displayed with bullet points
- `ordered list` : list format displayed with numbers or letters
- `description list` : list format for terms and their descriptions
- `nested lists` : hierarchical lists placed within other lists

### Important Notes
- `type` is a deprecated attribute for `<ul>` elements
- `value` attribute is for `<ol>` elements only


<hr>

## Block And Inline Elements

### All Tags
- `<div>` : a generic block-level container used for grouping content
    - `style` : applies CSS styles (like border, padding, or background) to the element
    - `class` : assigns a class name for CSS styling or grouping
    - `id` : assigns a unique identifier for an element
- `<p>` : block-level paragraph
- `<h1>` through `<h6>` : block-level headings
- `<ul>` : block-level unordered list
- `<ol>` : block-level ordered list
- `<form>` : block-level form container
- `<section>` : block-level structural container
    - `style` : same as `<div>`
- `<article>` : block-level structural content container
- `<span>` : inline container used for grouping or styling text
    - `style` : same as `<div>`
- `<a>` : inline link element
    - `href` : specifies the URL destination of the link
- `<strong>` : inline bold text
- `<em>` : inline italic text
- `<img>` : inline image element
- `<b>` : inline bold text
- `<i>` : inline italic text
- `<q>` : inline quotation
- `<abbr>` : inline abbreviation
    - `title` : provides the full text or meaning for the abbreviation

### Definitions
- `Block-level element` : creates a structural block of content, starts on a new line, and takes full width of the parent container
- `Inline element` : does not start on a new line and only takes up the width necessary for its content
- `Semantic element` : a tag that carries specific meaning about the content (e.g., `<section>`, `<article>`)

### Important Notes
- The CSS `display` property can override default element behavior (e.g., turning a block element into an inline element)
- Use semantic tags for structure instead of relying on generic `<div>` tags whenever possible
- Deprecated attributes like `align` or `width` should be replaced with CSS


<hr>

## Using the HTML `<iframe>` Element

### All Tags
- `<iframe>` : embeds an HTML document within the current document
    - `src` : specifies the URL of the content to embed
    - `width` : defines the iframe's width in pixels or percentages
    - `height` : defines the iframe's height in pixels or percentages
    - `name` : assigns a name to the iframe for targeting
    - `frameborder` : controls the border around the iframe
        - `0` : hides the border
        - `1` : displays the border
    - `allow` : specifies permissions for browser features
        - `autoplay` : allows media to start playing automatically
        - `fullscreen` : allows the iframe to enter fullscreen mode
        - `picture-in-picture` : allows floating video windows
        - `accelerometer` : grants access to device motion sensors
        - `gyroscope` : grants access to device orientation
        - `clipboard-write` : allows writing to the user's clipboard
        - `encrypted-media` : permits playing protected DRM content
        - `camera` : allows access to the user's camera
        - `microphone` : allows access to the user's microphone
        - `geolocation` : allows access to the user's location
        - `payment` : enables the Payment Request API
        - `usb` : allows interaction with USB hardware
        - `midi` : allows interaction with MIDI instruments
        - `display-capture` : enables screen sharing features
        - `web-share` : enables native share dialogs
    - `title` : provides a text description for accessibility
    - `sandbox` : security attribute used to restrict untrusted content
    - `allowfullscreen` : boolean attribute that enables fullscreen mode for the iframe
- `<a>` : anchor tag used to create links
    - `href` : specifies the destination URL of the link
    - `target` : specifies the target frame to load content, using the `name` of an `<iframe>`

### Definitions
- `inline frame` : another name for `<iframe>`, representing an isolated rectangular area for external content
- `sandbox` : a security feature used to isolate and restrict actions within an iframe

### Important Notes
- Always include a `title` attribute for accessibility
- Use the most restrictive permissions possible in the `allow` attribute; do not copy long lists blindly
- Use `sandbox` when embedding untrusted content
- Avoid loading too many iframes on a single page to maintain performance
- Modern browsers block powerful features (camera, microphone, etc.) by default; `allow` is required to grant permission


<hr>

## HTML Computer Code Elements

### All Tags
- `<code>` : used for inline computer code such as function names, variables, or short commands
- `<pre>` : used for preformatted text, preserving whitespace, tabs, and line breaks
- `<kbd>` : used for user input such as keyboard shortcuts, terminal commands, or button presses
- `<samp>` : used for sample output from a program, script, or system, such as console messages or logs
- `<var>` : used for variables or placeholders in code or mathematical expressions
- `<style>` : used to define CSS rules to enhance the appearance of elements

### Definitions
- `monospace font` : a font style where characters occupy the same horizontal space, used to distinguish technical content
- `semantic value` : the specific meaning or purpose an HTML element conveys to the browser and developer

### Important Notes
- Use `<pre>` for any content requiring exact whitespace or line breaks like code or ASCII art
- Use `&lt;` and `&gt;` for `<` and `>` in HTML snippets to prevent rendering issues
- Provide context in surrounding text to ensure accessibility for screen readers
- Use these elements only for technical content to maintain their semantic value.


<hr>

## HTML Semantic Elements

### All Tags
- `<article>` : defines independent, self-contained content
- `<aside>` : defines content indirectly related to the surrounding content, such as sidebars or pull quotes
- `<details>` : defines additional details that the user can toggle to view or hide
- `<figcaption>` : defines a caption for a `<figure>` element
- `<figure>` : specifies self-contained content like images, diagrams, or code
- `<footer>` : defines a footer for a document or section
- `<header>` : specifies introductory content for a document or section
- `<main>` : specifies the main content of a document
- `<mark>` : defines marked or highlighted text
- `<nav>` : defines a set of navigation links
- `<section>` : defines a thematic section in a document
- `<summary>` : defines a visible heading for a `<details>` element
- `<time>` : defines a specific date or time
    - `datetime` : attribute for machine-readable format of the date or time
- `<div>` : generic container (should be replaced by semantic elements when possible)
- `<span>` : generic inline container (should be replaced by semantic elements when possible)
- `<img>` : used to embed images
    - `src` : specifies the path to the image file
    - `alt` : provides alternate text for the image
    - `style` : applies CSS styles to the element
- `<video>` : used for video media
    - `src` : same as `<img>`
    - `controls` : boolean attribute that displays video player controls
- `<a>` : anchor tag used for links
    - `href` : specifies the URL destination of the link
- `<code>` : represents computer code

### Definitions
- `Semantic elements` : HTML5 elements that provide meaning to the structure of a web page, improving accessibility, SEO, and readability
- `Machine-readable format` : content structured so that it can be easily parsed by software (e.g., ISO dates)

### Important Notes
- Use semantic elements to replace generic `<div>` and `<span>` elements for better structure
- Content inside an `<article>` must be independent and reusable
- Include headings within `<section>` tags for thematic clarity
- Use only one `<main>` element per page
- Add the `datetime` attribute to `<time>` for machine-readable dates
- Semantic elements leverage improved accessibility (e.g., for screen readers) and SEO


<hr>

## HTML Entities and Symbols

### All Tags
- `<span>` : used to wrap text or entities for styling
    - `class` : assigns a CSS class name to the element
    - `aria-label` : provides a text label for accessibility, essential for screen readers to interpret emojis
    - `style` : applies inline CSS styles
- `<p>` : defines a paragraph of text
- `<style>` : defines CSS rules to enhance the appearance of elements

### Definitions
- `HTML Entity` : a string starting with `&` and ending with `;` used to display reserved characters or special symbols
- `Named Entity` : an entity using a descriptive name (e.g., `&copy;`)
- `Decimal Entity` : an entity using a decimal numeric code (e.g., `&#169;`)
- `Hexadecimal Entity` : an entity using a hex numeric code (e.g., `&#xA9;`)
- `Non-breaking space` : an entity (`&nbsp;`) that prevents line breaks between content

### Important Notes
- Use `&lt;`, `&gt;`, and `&amp;` for reserved characters to avoid HTML parsing errors
- Prefer named entities for readability; use hexadecimal or decimal for broader compatibility
- Add `aria-label` to emojis to improve accessibility for screen readers
- Stick to one entity format (named, hex, or decimal) within a project for consistency
- Use entities sparingly to maintain clean code.


<hr>

## HTML Forms and Input Elements

### All Tags
- `<form>` : container for user input controls
    - `action` : specifies the URL where form data is sent
    - `enctype` : specifies how form data is encoded
        - `application/x-www-form-urlencoded` : default encoding format for form data
        - `multipart/form-data` : required format for file uploads
        - `text/plain` : simple text format for data, rarely used
    - `autocomplete` : enables/disables autocomplete (Values: `on`, `off`)
    - `method` : specifies HTTP method (Values: `GET`, `POST`)
    - `name` : identifier for the form
    - `novalidate` : disables browser form validation
    - `target` : specifies where to display response (Values: `_blank`, `_self`, `_parent`, `_top`)
- `<input>` : defines an input control for user data
    - `type` : determines the control display (Values: `text`, `password`, `submit`, `radio`, `checkbox`, `button`, `color`, `date`, `datetime-local`, `email`, `file`, `hidden`, `image`, `month`, `number`, `range`, `reset`, `search`, `tel`, `time`, `url`, `week`)
    - `name` : name for the data field
    - `id` : unique identifier for the element
    - `value` : initial or submitted value of the input
    - `placeholder` : hint text displayed inside input
    - `size` : visible width in characters
    - `maxlength` : maximum allowed characters
    - `min` : minimum allowed value
    - `max` : maximum allowed value
    - `multiple` : allows multiple values to be selected
    - `pattern` : regex pattern for validation
    - `required` : makes the field mandatory
    - `step` : legal number intervals
    - `autofocus` : automatically focuses on element upon load
    - `height` : height dimension for images
    - `width` : width dimension for images
    - `list` : associates input with a `datalist`
    - `form` : connects input to a form ID outside the physical structure
    - `formaction` : overrides the form's `action`
    - `formmethod` : overrides the form's `method`
    - `formnovalidate` : disables browser validation for this specific button
    - `formtarget` : overrides the form's `target`
    - `formenctype` : overrides the form's `enctype`
    - `autocomplete` : same as `<form>`
    - `readonly` : makes input read-only
    - `disabled` : disables the input
- `<label>` : defines a label for form elements
    - `for` : matches the `id` of an associated input
- `<select>` : defines a drop-down list
    - `name` : same as `<input>`
    - `multiple` : same as `<input>`
    - `size` : same as `<input>`
- `<option>` : defines an option in a `select` or `datalist`
    - `value` : same as `<input>`
    - `selected` : pre-selects the option
    - `disabled` : same as `<input>`
- `<textarea>` : multi-line text input
    - `name` : same as `<input>`
    - `rows` : height in lines
    - `cols` : width in characters
    - `placeholder` : same as `<input>`
    - `readonly` : same as `<input>`
- `<button>` : clickable button
    - `type` : determines button behavior (Values: `button`, `submit`, `reset`)
    - `onclick` : JavaScript event handler
    - `form` : same as `<input>`
    - `formaction` : same as `<input>`
    - `formmethod` : same as `<input>`
    - `formnovalidate` : same as `<input>`
    - `formtarget` : same as `<input>`
    - `formenctype` : same as `<input>`
    - `name` : same as `<input>`
- `<fieldset>` : groups related elements
    - `disabled` : same as `<input>`
- `<legend>` : caption for `fieldset`
    - `style` : CSS styling
- `<datalist>` : list of pre-defined options for `input`
    - `id` : same as `<input>`
- `<optgroup>` : groups options within a `select`
    - `label` : display label for the group
- `<output>` : displays calculation or script output results
    - `name` : same as `<input>`

### Definitions
- `form` : container for input controls used to collect and submit user data
- `enctype` : specifies how form data is encoded/packaged before server transmission
- `GET` : HTTP method used to send data via URL parameters
- `POST` : HTTP method used to send data in the request body
- `form attribute` : allows an input or button to be associated with a form via ID even if placed outside the `<form>` element
- `formaction` : overrides the default URL destination of a form
- `formmethod` : overrides the default HTTP method of a form
- `formnovalidate` : disables browser/client-side validation for a specific submit button
- `formtarget` : overrides where the submission response is displayed

### Important Notes
- `enctype="multipart/form-data"` is strictly required for any form containing file uploads
- `formnovalidate` disables browser-side HTML validation but does not disable server-side validation
- The `form` attribute on `<input>` or `<button>` tags must reference the `id` of the corresponding `<form>` element