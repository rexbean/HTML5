- [Introduction](#introduction)
- [Structure](#structure)
  - [DOCTYPE](#doctype)
  - [head](#head)
- [Element](#element)
  - [Attributes](#attribute)
  - [Typical elements](#typicalElements)
    - [Headings](#headings)
    - [Comments](#comments)
    - [Paragraph](#paragraph)
    - [Links](#links)
    - [Formatting](#formatting)
    - [Image](#image)
    - [Table](#table)
    - [List](#list)
    - [Form](#form)
    - [Iframe](#iframe)
  - [Styles](#styles)
# <div id = "introduction">HTML introduction</div>
- HTML stands for **HyperText Markup language**. HTML is the basic building block of World Wide Web.
- **Hypertext** is text displayed on a computer or other electornic device with references to other text that the user can immediately access, usually by a mouse click or key press.
- **Markup Language** use set of markup tags to characterize text elements within a documents, which gives instructions to the web browsers on how the document should appear.
- **HTML** was originally developed by Tim Berners-Lee in 1990. In 1996, the **World Wide Web Consortium(W3C)** became the authority to maintain the HTML specifications.
HTML also became an **International Standard(ISO)** in 2000.
- **HTML5** provides a faster and more robust approach to web development.
# <div id = "structure">The structure of the HTML</div>
```html
<!DOCTYPE html>
<html lang = "en">
<head>
  <title>A simple HTML document</title>
</head>
<body>
  <p>Hello world!</p>
</body>
</html>
```
- **DOCTYPE declaration** is a line defines the HTML5 document type.
- **Head element** provides information about the document, including its title, style information and scripts.
- **Body element** contains the document's actual content that is rendered in the web browser and displayed to the user.
- **Other elements** consists of markup tags. Each markup tags is composed of a keyword, surrounded by angle brackes, like \<html\>, \</html\>. They always appear in pairs. They will be called opening tag and closing tag.
## Doctype
- Doctype declaration appears at the top of a web page before all other elements.
- The DOCTYPE for HTML5 is very short, and case-insensitive. The **Syntax** is `<!DOCTYPE html>`. But before it was longer, HTML language was SGML-based and required a reference to a DTD(Document Type Definition: This will tell what version of markup language the page is written in).
- This is only needed to enable the standard mode for the document.
## Head
- The head element describes properties of the document such as the **title, meta information, the location to find style sheets, the location of the scripts**
### Title &nbsp; `<title>`
- `<title>` defines the title of the document.
- Only one will be permitted and it must be placed within the head element.
- Different purposes:
  - To display in the title bar and in the task bar.
  - To provide title when added to favorites or bookmarked.
  - To display for the page in search-engine result.
### Base &nbsp; `<base>`
- `<base>` element is used to define the base URL for all relative links contained in the document.
  ```html
  <head>
    <title>Define a base URL</title>
    <base href = "http://www.abc.com/">
  </head>
  <body>
    <p><a href = "cdef/efg.html">Html</a></p>
  </body>
  ```
  The link will be `http://www.abc.com/cdef/efg.html`
### Link &nbsp; `<link>`
- `<link>` element defines the relationship between the current document and an external documents or resources. This commonly used to link external style sheets.
  ```html
  <head>
    <title>Linking to style sheets</title>
    <link type="text/css" rel="stylesheet" href="style.css">
  </head>
  ```
### Style &nbsp; `<style>`
- `<style>` element is used to define embedded style information for an HTML document.
- This define how the elements render in a browser.
  ```html
  <head>
    <title>Internal style sheet</title>
    <style type="text/css">
        body { background-color: YellowGreen; }
        h1 { color: red; }
        p { color: green; }
    </style>
  </head>
  ```
### Meta &nbsp; `<meta>`
- This will provide metadata about the HTML document, such as **keywords, description, author last modified and other metadata**.
- Metadata won't be show in the webpage, but it is machine parsable. It will be used for search engine or other web services.
- `name` is the key, `content` contains the value
- `charset` is used for setting the encoding for the HTML
- `keywords` and `description` is used to index web pages.
- `viewport` is used to enable zooming of website on mobile devices.
  ```html
  <head>
    <meta name="author" content="John Carter">
    <meta charset="UTF-8">
    <meta name ="viewport" content = "width=device-width, initial-scale=1">
    <title>Defining Document's Author</title>
  </head>
  ```
### Script &nbsp; `<script>`
- `<script>` element is used to define a client-side script, such as a JavaScript
- **client-side scripting** refers to the type of computer program that are executed by the user's web browser. JavaScript is the most popular one.
-
# <div id = "element">Element</div>
- HTML elements represent semantics, or meaning.
- HTML element always starts with opening tag and end with closing tag. The content is in the between.
- HTML element also contains **[attributes](#attribute)** to define the additional properties.
- Not all elements require the closing tag. That kind of element is called **Empty element**, **self-closing** or **void elements**. They are not container tags, which means no content, like \<br\>.
- **Element** is the same thing with **HTML tag**
- The tags and attributes are **case insensitivity**.
- Elements can contain any number of further elements, which means nested.`<p class = "example">Here is some <em>emphasized</em> text.</p>`
- **HTML Elements Types:** can be divided into two distinct groups: **[block level](#blockLevel)** and **[inline level](#inlineLevel)**. The former make up the document's structure and latter dress up the contents of a block.
## <div id = "attribute">Attributes</div>
- Attribute is used to define additional properties of an element.
- Most attributes requires a value and it is recommended to enclose attribute values in quotes.
- If the value has the quotes, it should be wrapped by **single quotes**
- **[HTML5 has global attributes](#globalAttributes)**
- **[HTML5 has event attributes](#eventAttributs)**
## <div id = "typicalElements">Typical Elements</div>
### <div id = "comments">Comments</div>
- In HTML uses `<!--` and `-->`to wrap the comments.
### <div id = "headings">Headings &nbsp;\<h1\> to \<h6\></div>
- HTML uses six levels of heading tags \<h1\> to \<h6\>, \<h1\> is the most important one.
- Browser built-in style sheets automatically create some empty space before and after each heading.
- As search engines use headings to index the structure and content of web pages
### <div id = "paragraph">Paragraph &nbsp;\<p\></div>
- `<p>` tag is used to define the paragraph.
- Browser will ignore the empty paragraph `<p></p>`.
- `<br>` tag is used to insert a line break.
### <div id = "links">Links &nbsp;\<a\></div>
- Links allow users to move seamlessly from one page to another.
- Link has two ends. One is called anchor and the other is a direction. The link starts at the source anchor and points to the destination anchor.
- There are three kinds of appearance of links in browser
  - **Unvisited link** is underlined with blue
  - **Visited link** is underlined with purple
  - **Active link** is underlined with red
- The **Syntax** of link is `<a href = "url">Text link</a>` and **href** in source anchor specifies the address of the **destination anchor**.
- The **target attribute** is used to tell the browser where to open the linked document.**(_blank, _parent, _self, _top)**.
- **`id`** attribute in any elements can be used as the bookmark. The anchor can use `href = "#<IdName>"`to jump to their.
- Putting the address of the file in the `href` attribute can be used as the link for downloading.
### <div id = "formatting">Formatting</div>
#### Text formatting
- There are a lot of tags can be used to format the text.
- Examples code here:

| Source code                                               | Results                                                 |
| ----------------------------------------------------------| ------------------------------------------------------- |
| `<b>This text is bold</b>`                                | <b>This text is bold</b>                                |
| `<code>This is computer code</code>`                      | <code>This is computer code</code>                      |
| `<em>This text is emphasized</em>`                        | <em>This text is emphasized</em>                        |
| `<i>This text is italic</i>`                              | <i>This text is italic</i>                              |
| `<small>This text is small</small>`                       | <small>This text is small</small>                       |
| `<mark>This text is marked</mark>`                        | <mark>This text is marked</mark>                        |
| `<strong>This text is strongly emphasized</strong>`       | <strong>This text is strongly emphasized</strong>       |
| `This is <sub>subscript</sub> and <sup>superscript</sup>` | This is <sub>subscript</sub> and <sup>superscript</sup> |
| `<ins>This text is inserted to the document</ins>`        | <ins>This text is inserted to the document</ins>        |
| `<del>This text is deleted from the document</del>`       | <del>This text is deleted from the document</del>       |
#### Citations, Quotations and Definition
| Tag            | Description                      | Example                                | Attribute        |
| -------------- | -------------------------------- | -------------------------------------- | ---------------- |
| \<abbr\>       | Defines an abbreviation          | `<abbr title = xxx>HTML</abbr>`        | `title = ..`     |
| \<address\>    | Defines contact information      | `<footer><address></address></footer>` | global           |
| \<bdo\>        | Defines the text direction       | `<bdo dir = "ltr">1-2-3-4-5</bdo>`     | `dir = ltr/rtl`  |
| \<blockquote\> | indicates block-level quotation  | `<blockquoate>...</blockquote>`        | `cite = "<URL>"` |
| \<q\>          | indicates short inline quotation | `<q>...</q>`                           | `cite = "URL"`   |
| \<cite\>       | Define a citation                | `<cite>...</cite>`                     | global           |
| \<dfn\>        | Define a definition term         | `<dfn title = "xxx">HTML</dfn>`        | `title = ".."`   |
#### Computer Output
| Tag      | Description                                                     | Example                   |
| -------- | --------------------------------------------------------------- | ------------------------- |
| \<code\> | computer code text                                              | `<code><pre></pre><code>` |
| \<kbd\>  | indicate the user input                                         | `<kbd>...</kbd>`          |
| \<samp\> | indicate the general Output                                     | `<samp>..</samp>`         |
| \<var\>  | indicate instance of variable                                   | `<var>x</var>`            |
| \<pre\>  | define preformatted text<br> to preserve space, line break, tab | `<pre>...</pre>`          |
### <div id = "image">Image &nbsp;\<a\> \<map\> \<area\></div>
- `<img>` tag is used to insert images in the HTML. It is an empty element and contains attribute only.
- The **syntax** is `<img src = "url" alt = "some_text">`
- `src` attribute points to the location of the image
- `alt` attribute is used to be the alternative description for an image.(slow connection, an error)
- `width` and `height` are used to specify the width and height of the image, all are specified in **pixels** by default, without these two attributes image will be shown in original size
- `<map>` is used to give the image different hyperlink areas without dividing the image into separated images.
  - The `name` of the `<map>` is correponding to the `usermap` attribute of the `<img>`
- `<area>` defines a hot-spot region on an image, and associates it with a hypertext link. It must be used in `<map>` element
```html
<img src = "abc.png" usemap = "#shapes" alt = "Geometrical Shapes">
<map name = "shapes">
  <area shape = "circle" coords = "40,40,40" href = "circle.html" alt ="Circle">
  <area shape = "poly" coords = "148,2,104,80,193,80" href = "triangle.html" alt = "Triangle">
  <area shape = "rect" coords = "226,2,323,80" href = "rectangle.html" alt = "Rectangle">
  <area shape = "poly" coords = "392,2,352,32,366,80,418,80,432,32" href = "pentagon.html" alt = "Pentagon">
</map>
```
### <div id = "table">Table</div>
#### Tags
- `<table>` is used to define a table in HTML.
- `<tr>` is used for a row.
- `<td>` is used for each cell.
- `<th>` is used for the header.
#### Attributes
- `border` is used to set the border width
- `cellpadding` is used to define the space betweeen border and the content
- `cellspacing` is used to define the space between cells
- `rowspan` and `colspan` can be used to extend row and column to multiple ones.
#### Example
```html
<table>
  <thead>
    <tr>
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tr>
    <td>sss</td>
    <td colspan = "2">aaa</td>
  <tr>
</table>
```
<table>
  <thead>
    <tr>
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tr>
    <td>sss</td>
    <td colspan = "2">aaa</td>
  <tr>
</table>

### <div id = "list">List</div>
- List is used to present list of information in well formed and semantic way.
- There are three types of lists:
  - **Unordered list**: Used to group a set of related items, in no particular order.
  - **Ordered List**: Used to group a set of related items, in a specific order.
  - **Description List**: Used to display a list of terms and their descriptions.
- List can be nested.
#### Unordered List &nbsp; \<ul\>
- \<ul\> is used to create unordered list and \<li\> is for the list item
- Each \<li\> will be marked with bullets
#### Ordered List &nbsp; \<ol\>
- \<ol\> is used to create ordered list and \<li\> is also for the list item
- Each itme will be marked with a number
#### Description List &nbsp; \<dl\>
- \<dl\> is used to create a description list.
- \<dt\> is for the term
- \<dd\> is for the description

### <div id = "form">Form</div>
- `Form` is used to collect different kinds of user inputs.
- Form can contain different elements called controls like **inputbox, checkboxeds, radio-buttons, submit buttons,etc**
- `<form>` is used to create HTML form
#### Input Elements
- `<input>` is used to define **Input elements**
- `<label>` is used to lables for `<input>` elements, linked by `id` attribute
##### Text fields
- One line areas that allow the user to input text.
  ```html
  <form>
    <label for = "username">Username:</label>
    <input type="text" name = "username" id = “username”>
  </form>
  ```
  <form>
    <label for = "username">Username:</label>
    <input type="text" name = "username" id = “username”>
  </form>
##### Password Field
- Characters in a password field are masked, like asterisks or dots
  ``` html
  <form>
    <label for="user-pwd">Password:</label>
    <input type="password" name="user-password" id="user-pwd">
  </form>
  ```
  <form>
    <label for="user-pwd">Password:</label>
    <input type="password" name="user-password" id="user-pwd">
  </form>
##### Radio Buttons
- Let user select exactly one option from a pre-defined set of options.
  ```html
  <form>
      <input type="radio" name="sex" id="male">
      <label for="male">Male</label>
      <input type="radio" name="sex" id="female">
      <label for="female">Female</label>
  </form>
  ```
  <form>
      <input type="radio" name="sex" id="male">
      <label for="male">Male</label>
      <input type="radio" name="sex" id="female">
      <label for="female">Female</label>
  </form>
##### Checkboxes
- Allow user to select one or more options from a pre-defined set of options.
  ``` html
  <form>
    <input type="checkbox" name="sports" id="soccer">
    <label for="soccer">Soccer</label>
    <input type="checkbox" name="sports" id="cricket">
    <label for="cricket">Cricket</label>
    <input type="checkbox" name="sports" id="baseball">
    <label for="baseball">Baseball</label>
  </form>
  ```
  <form>
    <input type="checkbox" name="sports" id="soccer">
    <label for="soccer">Soccer</label>
    <input type="checkbox" name="sports" id="cricket">
    <label for="cricket">Cricket</label>
    <input type="checkbox" name="sports" id="baseball">
    <label for="baseball">Baseball</label>
  </form>
##### File Select box
- Browser for a local file and send it as an attachment to the form data
  ```html
  <form>
    <label for="file-select">Upload:</label>
    <input type="file" name="upload" id="file-select">
  </form>
  ```
  <form>
    <label for="file-select">Upload:</label>
    <input type="file" name="upload" id="file-select">
  </form>
##### Textarea
- Multiple-line text input control that allows a user to enter more than one line of text.
  ```html
  <form>
    <label for="address">Address:</label>
    <textarea rows="3" cols="30" name="address" id="address"></textarea>
  </form>
  ```
  <form>
    <label for="address">Address:</label>
    <textarea rows="3" cols="30" name="address" id="address"></textarea>
  </form>
##### Select Boxes
- It is a dropdown list of options that allows user to select one or more option from a pull-down list of options.
  ```html
  <form>
    <label for="city">City:</label>
    <select name="city" id="city">
        <option value="sydney">Sydney</option>
        <option value="melbourne">Melbourne</option>
        <option value="cromwell">Cromwell</option>
    </select>
  </form>
  ```
  <form>
    <label for="city">City:</label>
    <select name="city" id="city">
        <option value="sydney">Sydney</option>
        <option value="melbourne">Melbourne</option>
        <option value="cromwell">Cromwell</option>
    </select>
  </form>
##### Submit and Reset Buttons
- `Submit` button is for sending data,
- `Reset` button is for reset the control to default values
- These can be replaced by `<button>` element
  ```html
  <form action="action.php" method="post" id="users">
    <label for="first-name">First Name:</label>
    <input type="text" name="first-name" id="first-name">
    <input type="submit" value="Submit">
    <input type="reset" value="Reset">
  </form>
  ```
  <form action="action.php" method="post" id="users">
    <label for="first-name">First Name:</label>
    <input type="text" name="first-name" id="first-name">
    <input type="submit" value="Submit">
    <input type="reset" value="Reset">
  </form>
#### Attributes
- `name` is the name of the form, using `id` now
- `action` is the URL of submitted address
- `method` is the Type of the HTTP method: `GET`,`POST`,`PUT`,`DELETE`
- `target` is the place where to open the result
### <div id = "iframe">iFrame</div>
- An iframe or inline frame is used to display external objects including other web pages within a web page.
- The **syntax** is used to create iframe
  ```html
  <iframe src = "URL">
    alternative content for browser which do not support iframe.
  </iframe>
  ```
- `width` and `height` are used to specify the width and height of the iframe
- `frameborder` can be set 0 or 1, 0 can remove the border from the iframe
- `iframe` can be used as a target for the hyperlinks, by using `name` as reference
  ```html
  <iframe src = "demo-page.html" name = "myFrame"></iframe>
  <p><a href = "abc.com" target = "myFrame">abc</a></p>
  ```
