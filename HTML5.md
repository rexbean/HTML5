# HTML 5
- [Introduction](#introduction)
- [Structure](#structure)
- [Element](#element)
  - [Attributes](#attribute)
  - [Typical elements](#typicalElements)
    - [Headings](#headings)
    - [Comments](#comments)
    - [Paragraph](#paragraph)
    - [Links](#links)
    - [Formatting](#formatting)
## <div id = "introduction">HTML introduction</div>
- HTML stands for **HyperText Markup language**. HTML is the basic building block of World Wide Web.
- **Hypertext** is text displayed on a computer or other electornic device with references to other text that the user can immediately access, usually by a mouse click or key press.
- **Markup Language** use set of markup tags to characterize text elements within a documents, which gives instructions to the web browsers on how the document should appear.
- **HTML** was originally developed by Tim Berners-Lee in 1990. In 1996, the **World Wide Web Consortium(W3C)** became the authority to maintain the HTML specifications.
HTML also became an **International Standard(ISO)** in 2000.
- **HTML5** provides a faster and more robust approach to web development.
## <div id = "structure">The structure of the HTML</div>
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
## <div id = "element">Element</div>
- HTML elements represent semantics, or meaning.
- HTML element always starts with opening tag and end with closing tag. The content is in the between.
- HTML element also contains **[attributes](#attribute)** to define the additional properties.
- Not all elements require the closing tag. That kind of element is called **Empty element**, **self-closing** or **void elements**. They are not container tags, which means no content, like \<br\>.
- **Element** is the same thing with **HTML tag**
- The tags and attributes are **case insensitivity**.
- Elements can contain any number of further elements, which means nested.`<p class = "example">Here is some <em>emphasized</em> text.</p>`
- **HTML Elements Types:** can be divided into two distinct groups: **[block level](#blockLevel)** and **[inline level](#inlineLevel)**. The former make up the document's structure and latter dress up the contents of a block.
### <div id = "attribute">Attributes</div>
- Attribute is used to define additional properties of an element.
- Most attributes requires a value and it is recommended to enclose attribute values in quotes.
- If the value has the quotes, it should be wrapped by **single quotes**
- **[HTML5 has global attributes](#globalAttributes)**
- **[HTML5 has event attributes](#eventAttributs)**
### <div id = "typicalElements">Typical Elements</div>
#### <div id = "comments">Comments</div>
- In HTML uses `<!--` and `-->`to wrap the comments.
#### <div id = "headings">Headings &nbsp;\<h1\> to \<h6\></div>
- HTML uses six levels of heading tags \<h1\> to \<h6\>, \<h1\> is the most important one.
- Browser built-in style sheets automatically create some empty space before and after each heading.
- As search engines use headings to index the structure and content of web pages
#### <div id = "paragraph">Paragraph &nbsp;\<p\></div>
- `<p>` tag is used to define the paragraph.
- Browser will ignore the empty paragraph `<p></p>`.
- `<br>` tag is used to insert a line break.
#### <div id = "links">Links &nbsp;\<a\></div>
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
#### <div id = "formatting">Formatting</div>
##### Text formatting
- There are a lot of tags can be used to format the text.
- Examples code here:

| Source code                                                      | Results                                                        |
| ---------------------------------------------------------------- | -------------------------------------------------------------- |
| `<b>This text is bold</b>`                                 | <b>This text is bold</b>                                |
| `<code>This is computer code</code>`                      | <code>This is computer code</code>                    |
| `<em>This text is emphasized</em>`                        | <em>This text is emphasized</em>                        |
| `<i>This text is italic</i>`                              | <i>This text is italic</i>                              |
| `<small>This text is small</small>`                       | <small>This text is small</small>                       |
| `<mark>This text is marked</mark>`                        | <mark>This text is marked</mark>                       |
| `<strong>This text is strongly emphasized</strong>`       | <strong>This text is strongly emphasized</strong>       |
| `This is <sub>subscript</sub> and <sup>superscript</sup>` | This is <sub>subscript</sub> and <sup>superscript</sup>|
| `<ins>This text is inserted to the document</ins>`        | <ins>This text is inserted to the document</ins>        |
| `<del>This text is deleted from the document</del>`                                                                 | <del>This text is deleted from the document</del>                                                             |
##### Citations, Quotations and Definition
| Tag         | Explanination               | Example                                | Attributes |
| ----------- | --------------------------- | -------------------------------------- | ---------- |
| \<abbr\>    | Defines an abbreviation     | `<abbr title = xxx>HTML</abbr>`        | global     |
| \<address\> | Defines contact information | `<footer><address></address></footer>` | global     |
| \<bdo\>     | Defines the text direction  | `<bdo dir = "ltr">1-2-3-4-5`           | `dir = ltr/rtl` override the current directionality of text           |
