##### Full Form of HTML
Hyper Text Markup Language

##### What does Hyper Text means?
**Hyper Text** is a text which contains links to other texts.

##### What does Markup Language means?
A **markup** **language** is a [text-encoding system](https://en.wikipedia.org/wiki/Encoding "Encoding") which specifies the structure and formatting of a document and potentially the relationships among its parts. Markup can control the display of a document or enrich its content to facilitate automated processing. It's a way to give instructions to a computer about how to display and organize content.

Example => of `<p></p>` tag and `<strong></strong>` tag.
<p> This is a <strong> bold </strong> text.</p>
### History of HTML

The concept of *hypertext* was proposed by computer scientist Ted Nelson in the 1960's. 

Tim Berners-Lee, a British Computer Scientist introduced the WWW
World Wide Web, developed the first html website.

HTML 2.0 , HTML 3.2, HTML 4.0 

HTML 5.0 

#### Syntax
```html
<h1> HTML </h1>
```
- opening tag `<h1>`
- closing tag `</h1>`
- content `HTML`
- HTML elements => `<h1> HTML </h1>`

###### HTML TIPS 
The file extension must be .html or .htm
MS-DOS and Windows 3.1 had limitations on the number of characters in a filename. (.exe, .bat, .bat, .zip, .txt)

The file name must be index.html because it's default path of our homepage or the root of our website.

## HTML Documents / Structure
```html
<!DOCTYPE html>
<html>
	<head>
		<title> Home Page </title>
     </head>
     <body>
	     <h1> Best </h1>
	</body>
</html>
```
- <!DOCTYPE html> => tells the version of html that will be used in the html document, mostly it's for HTML 5.
- html => root of an HTML document
- head => information about the html document
- title => title of the html document
- body => contains everything you want to display on the web page.

## How browsers determine the language of an HTML document ?

`<html lang="en">`

lang attribute specifies the language of the content.
"en" => language code for the content, "hi" => for hindi

**Attributes** are used along with the html tags to define the characteristics of the element. They provide additional information about elements.

### in Hindi
```html
<!DOCTYPE html>
<html lang="hi">
<head>
	<meta charset="UTF-8">
	<title> Hindi Example </title>
<head>
<body> 
	<p> ये एक उदाहरण है हिन्दी मे कैसे लिखें </p>
</body>
</html>
```

## HTML Heading & Text
- Headings (`<h1> to <h6>`)
- Paragraphs (`<p>`)
- Line breaks (`<br>`)
- Horizontal rule (`<hr>`)

### HTML Headings
<h1> Heading h1 </h1>
<h2> Heading h2 </h2>
<h3> Heading h3 </h3>
<h4> Heading h4 </h4>
<h5> Heading h5 </h5>
<h6> Heading h6 </h6>
A single `<h1>` is typically used per page.
follow the hierarchy `<h1>` to `<h6>`

### HTML Paragraphs

<p>paragraph</p>
`<p></p>`

Browser automatically adds a single blank before and after `<p>` `</p>` tag.
Note: Block level elements cannot nest block elements but can nest inline elements like `<strong>` `<em>` etc.

### Working with br and hr tags

`<hr />` => horizontal rule or thematic break in paragraph level elements.

`<br />` => line break in text (carriage return)

 No matter how many ==white-space== you use inside HTML elements or content, the html parser reduces each sequence of ==white-space== to single space when rendering the code. 

### Comments

`<!-- comment -->`

like this you can comment in html

### Text Formatting

- bold => `<strong>`, `<b>`
- italic => `<em>`, `<i>`
- underline => `<u>` `<s>` -> ~~Strike~~ no longer relevant
- subscript => `<sub>`
- superscript => `<sup>`
- Examples =>

<html>
	<head>
		<title>Example</title>
	</head>
	<body>
		<p><strong>hi</strong></p>
		<p><em>there</em></p>
		<p><u>are</u></p>
		<p><s>you</s></p>
		<p>good<sub>1</sub></p>
		<p>hahaha<sup>2</sup></p>
	</body>
</html>

```html
<html>
	<head>
		<title>Example</title>
	</head>
	<body>
		<p><strong>hi</strong></p>
		<p><em>there</em></p>
		<p><u>are</u></p>
		<p><s>you</s></p>
		<p>good<sub>1</sub></p>
		<p>hahaha<sup>2</sup></p>
	</body>
</html>
```


##### Preformatted text
- `<pre>` => it will show as it is the content is.
- `<kbd>` => used to represent something related to a command or keyboard usage .
- `<abbr>` => see full form of any short abbreviation or acronym {title attribute}
- `<mark>` => highlight your text
- `<small>` => make text small
- `<del>` => used as a strike removal from document

<html>
	<head>
		<title>Example</title>
	</head>
	<body>
		<pre>
			<kbd>Ctrl</kbd>+<kbd>s</kbd>
			<abbr title="Control">Ctrl</abbr>
			<mark>Highlight</mark>
			<p>big<small>small text</small></p>
			<p>hi <del>no</del></p>
		</pre>
	</body>
</html>

```html
<html>
	<head>
		<title>Example</title>
	</head>
	<body>
		<pre>
			<kbd>Ctrl</kbd>+<kbd>s</kbd>
			<abbr title="Control">Ctrl</abbr>
			<mark>Highlight</mark>
			<p>big<small>small text</small></p>
			<p>hi <del>no</del></p>
		</pre>
	</body>
</html>
```

### Inline Styling
<p style = "color: blue">hello</p> 

```html
<p style = "color: blue">hello</p> 
```

#Note => While using nested tags never mismatch the tags

## Anchor Tag

`<a>` => anchor tag is used to create hyperlink, link one page to another

```html
<a href="https://www.example.com/">visit</a>
```

<a href="https://www.example.com/">visit</a>

<abbr title="Hypertext Reference">href</abbr> => hyper text reference

URL => Uniform Resource Locator
