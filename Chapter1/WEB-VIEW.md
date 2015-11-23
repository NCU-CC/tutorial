# WEB-VIEW
this section is talking about frontend view of web

## Table of Contents
- [View](#View)
- [HTML](#HTML)
- [XML](#XML)
- [JSON](#JSON)
- [Comparison](#Comparison)
- [References](#References)

## View
We can format a resource in many ways. For example, We can use HTML to represent a website. However, HTML is too heavy to transfer simple data ( e.g. user name ). We must find other ways to do so. A solution is using `XML` and `JSON`

## HTML
HTML ( HyperText Markup Language ) is used to create web pages.
All websites you see from browser is rendered in HTML.

### HTML Examples

The following example can show up a page with title `This is a title` and content `Hello world!` if you save it as `.html` file and open it with browser

```html
<html>
  <head>
    <title>This is a title</title>
  </head>
  <body>
    <p>Hello world!</p>
  </body>
</html>
```

### HTML Purpose
HTML can be rendered with `css` and `javascript` as a pretty website and this is its only purpose

## XML
XML ( Extensible Markup Language  ) can represent a nested structure. HTML is formatted in XML!

### XML Examples
```xml
<?xml version="1.0" encoding="UTF-8"?>
<book>
  <chapter id="1">
    <name>first</name>
  </chapter>
  <chapter id="2">
    <name>second</name>
  </chapter>
</book>
```

### XML Format

- Declaration : declare some information about itself

    `<?xml version="1.0" encoding="UTF-8"?>`

- Tag : begins with **<** and ends with **>**
  - start-tags : `<section>`
  - end-tags : `</section>`
  - empty-element tags : `<section />`

- Element :

  a component which either
  - begins with a **start-tag** and ends with a matching **end-tag**
  ```xml
  <Greeting>
  </Greeting>
  ```

  - consists only of an **empty-element tag**
  ```xml
  <line-break />
  ```

  data *between start and end tag* is its content which may contain  `text` or `element`

  ```xml
  <Greeting>
    Hello, world
    <line-break />
  </Greeting>
  ```

  ```xml
  <book>
    <chapte>
      <name>first</name>
    </chapter>
  </book>
  ```

- Attribute : a name / value pair that exists within a `start-tag` or `empty-element` tag
  ```xml
  <img src="madonna.jpg" alt='Foligno Madonna, by Raphael' />
  ```

### XML Purpose
XML is used to carry data


## JSON
JSON（ JavaScript Object Notation ） can represent a nested structure and easy to read

### JSON Examples
```json
{
  "book": {
    "chapter": [
      {
        "id": "1",
        "name": "first"
      },
      {
        "id": "2",
        "name": "second"
      }
    ]
  }
}
```

### JSON Format
- Number  : a signed decimal number

  `15`

- String  : a sequence of Unicode characters, delimited with double-quotation ( `""` )

  `"key"`

- Boolean : either of the values `true` or `false`

  `true`

- Array   : an ordered list, each of which may be of any type. Arrays use square bracket ( `[]` ) notation with elements being comma-separated ( `,` )

  `[ 1, 2, 3 ]` `[ "a", "b" ]`

- Object  : unordered collection of key / value pairs where the **keys are strings**, delimited with curly brackets ( `{}` ) and use commas ( `,` ) to separate each pair

  ```json
  {
    "id" : 1,
    "name" : "JasonChiu"
  }
  ```

### JSON Purpose
JSON is also used to carry data but more light-weighted

## Comparison
compare between `XML` and `JSON`

### JSON Comparison
- Pro
  - simple syntax
  - easy to use in javascript
- Con
  - less data types are supported

### XML Comparison
- Pro
  - possible to create dialects
  - built in support for namespaces
- Con
  - wordy

## References
- https://en.wikipedia.org/wiki/HTML
- https://en.wikipedia.org/wiki/XML
- https://en.wikipedia.org/wiki/JSON
- http://stackoverflow.com/questions/4862310/json-and-xml-comparison
