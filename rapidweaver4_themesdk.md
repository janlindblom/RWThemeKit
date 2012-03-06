# RapidWeaver 4 Theme SDK

## Realmac Software Theme Tutorial: Table of Contents
* [**RapidWeaver 4.0 Theme Tutorial**](#sect1)
 * [Requirements](#sect11)
 * [Before you start](#sect12)
* [Installing Your Theme](#sect2)
 * [Access The Files](#sect21)
* [**The Basics**](#sect3)
* [HTML](#sect30)
 * [Semantics](#sect31)
 * Tags
 * Attributes
 * ID's and Classes
 * Div's and Span's
 * Basic Page Structure
 * Summary
* CSS
 * CSS Selectors
 * Global Selectors
 * Class Selectors
 * ID Selectors
 * Nested Styles
 * Linking the styles.css file to index.html
 * Summary
* **Rapidweaver Templates**
 * The index.html file
 * Document Structure
* RapidWeaver Syntax Tags
 * The %pathto(...)% Tag
* CSS Selectors and the index.html file
 * Linking the styles.css file to index.html
* **Styling Your Theme**
 * Common Styling
 * Link Styling
 * Site Width
 * Content and Sidebar
 * Clearers
 * Content Padding
 * Page Header
 * Title and slogan
 * Navigation Styling
 * Default Styles
 * Current Link Styling
 * Footer Styling
 * Applying a background image
 * Adding A Theme Preview
* Conclusion
 * Useful CSS Links
* Appendix
 * SDK Appendix

[sect1]: <#sect1> "RapidWeaver 4.0 Theme Tutorial"
[sect11]: <#sect11> "Requirements"
[sect12]: <#sect12> "Before you start"
[sect2]: <#sect2> "Installing Your Theme"
[sect21]: <#sect21> "Access The Files"
[sect3]: <#sect3> "The Basics"
[sect30]: <#sect30> "HTML"
[sect31]: <#sect31> "Semantics"

## <a name="#sect1">RapidWeaver 4.0 Theme Tutorial</a>
Welcome to the Realmac Software Theme SDK, the aim of this tutorial is to give you a basic understanding of how you can build a unique theme for RapidWeaver. You'll learn about theme syntax, the property list file and how it controls your theme, how themes are structured and some basic styling.

### <a name="#sect11">Requirements</a>
* RapidWeaver 4.0 or newer (RapidWeaver 3.6 is available for those not using Leopard)
* A text editor (TextWrangler or similar)
* A CSS Editor (CSSEdit or similar) recommended
* Skill Level: RapidWeaver / Web enthusiast. Basic XHTML and CSS knowledge an advantage.
* Objectives: To gain an understanding of how RapidWeaver themes are constructed and learn some basic CSS styling for the theme.
* Time: 1 - 2 hours depending on skill level.

### <a name="#sect12"></a>Before you start
Before you start you need to make sure you have RapidWeaver 4.0 or newer installed. You can download the latest version of RapidWeaver from [http://www.realmacsoftware.com](http://www.realmacsoftware.com). This tutorial has been designed and written for 4.0, however it is perfectly apt for use with 3.6 as the theme structure and development process is identical.

You'll also need a text editor, TextWrangler from Bare Bones Software ([http://www.barebones.com](http://www.barebones.com)) is free and provides syntax highlighting which makes reading large amounts of code infinitely easier. Alternatively you can use TextEdit which is shipped with the Mac.

Finally a good CSS editor will also come in very useful. I recommend you buy a license for CSSEdit from MacRabbit [http://macrabbit.com](http://macrabbit.com), it's not essential but it makes CSS coding a breeze!

With everything in place, let's get started...

## Installing Your Theme
Install the Tutorial.rwtheme file by double-clicking it. You then need to restart RapidWeaver for the theme to become active.
 
### Access The Files
Once you have the theme installed, open the Tutorial Site project file by double clicking it, once RapidWeaver has loaded choose the tutorial theme from the theme drawer. Right click on the theme preview and select Show Contents.

This will reveal a Contents folder in the finder, inside are all the files required to construct a RapidWeaver theme. You should have the following files:

* **index.html** - layout template file (XHTML) 
* **styles.css** - base stylesheet (CSS) 
* **colourtag.css** - colour style variations stylesheet (CSS) 
* **print.css** - print stylesheet, styles the layout of your page when printed (CSS) 
* **handheld.css** - handheld device, styles the layout of your page when viewed on a mobile device (CSS) 
* **javascript.js** - required javascript for the theme 
* **images** - where all images for the theme are placed 
* **css folder** - theme variations CSS files are placed in here, such as sidebar location, page-width etc. 
* **preview.png** - 115x125px image/logo of your theme displayed in the theme drawer. (Version 3.6 and under)
* **preview_large.jpg** - 800x950px image/logo of your theme displayed in the theme drawer. (version 4.0 and up)

## The Basics
Firstly before we begin any work on the theme it is important to understand the fundamentals of a website. This chapter will cover basic XHTML and CSS as well as the general workings of a webpage. If you are comfortable with these areas then you may wish to skip this chapter.

### HTML
#### Semantics
When designing any webpage it is important to use valid XHTML your .html pages should contain all the vital information you wish to communicate to your viewer. All other code such as styling and javascript should be contained in external files and linked into your document. The idea behind this is to ensure that if your page was viewed with no styling it reads easily and clearly.

#### Tags 
HTML uses tags to mark up areas of the page to ensure the browser reads it correctly. For example a &lt;h1&gt; tag denotes a heading, this will be displayed more prominently on the page with a larger bold font.

Tags nearly always have both opening - &lt;p&gt; - and closing - &lt;/p&gt; -mark-up, closing tags are prefixed with a forward slash /. For example a paragraph will be displayed as follows. 

	<p>This is a paragraph!</p>

#### Attributes
Tags can also be assigned attributes, these reside inside the opening tag and can be used to assign extra information to your code. For example a link can be marked up as follows.

	<a href=”http://www.realmacsoftware.com” title=”Visit the Realmac Homepage”>Visit the Realmac Homepage</a>

Notice the **href** and **title** inside the &lt;a&gt; tag. The href specifies the url the link is to go to, the title attribute gives a textual description of the urls destination.

#### ID's and Classes
A couple of other important attributes are ID's and Classes these can be used to assign meaning to certain parts of your page. More importantly they are used alongside CSS to specify specific areas for styling. A list of links that you wish to use for navigation could be marked up as follows;

	<ul id=”navigation”>
		<li><a href=”page1.html”>Home</a></li>
		<li><a href=”page2.html”>Page 2</a></li>
		<li><a href=”page3.html”>Page 3</a></li>
	</ul>

Don’t worry too much if this doesn't make sense just yet, we will return to this in the tutorial.

#### Div's and Span's
Finally the last section of this chapter focus' on &lt;div&gt; and &lt;span&gt; tags, &lt;div&gt;'s especially are used quite frequently in the theme template. A &lt;div&gt; is a block element, this means that any content inside the tag will be moved onto a new line and automatically take up the full width of the page, just like a &lt;p&gt; or &lt;h1&gt; tag.

A &lt;span&gt; is an inline element, this does not disrupt the flow of the page but instead will flow with the text in the same way as &lt;b&gt;, &lt;i&gt; or &lt;a&gt; tags.

Whilst not having a great amount of semantic meaning, &lt;div&gt;'s can be used to mark out areas of your site to allow easy styling with CSS. For example the following image illustrates a common site layout. One which we will use in the tutorial. It can be broken down into five distinct areas;

* Container
* Page
* Header
* Content
* Sidebar
* Footer

[[ figure 1]]

These can be marked out accordingly with XHTML;
￼
	<div id=”container”>
		<div id=”header”>Header </div>
		<div id=”content”>Content</div>
		<div id=”sidebar”>Sidebar</div>
		<div id=”footer”>Footer</div>
	</div>

Notice the four distinct sections are wrapped in an outer container, this make it easier to set an overall site width. **ID** attributes are also used to identify the regions.

#### Basic Page Structure
Now we have seen how &lt;div&gt;'s can be used to mark out the content areas of the page we can focus on how this is inserted into a working **.html** page that can be viewed by a browser.

There are two main areas of an **XHTML** document, the &lt;head&gt;, which contains all the information required before the page loads such as page title and stylesheets. Second is the &lt;body&gt; this contains anything you wish to be visible to the user.

The &lt;body&gt; and &lt;head&gt; tags are wrapped in an &lt;html&gt; tag, this tells the browser that we want to render the page as &lt;html&gt;. All of this is preceded by a &lt;DOCTYPE&gt; declaration. This statement tells the browser that we would like our page to be rendered as valid XHTML. By ensuring our page validates we can ensure that the page will display as intended across all modern browsers.

The code on the following page illustrates the standard mark-up for a basic **XHTML** page including our seg- mented page layout.

The observant among you may have noticed a &lt;link&gt; tag in the &lt;head&gt;, this imports all of our styles into our page. We will cover this in greater detail later in the tutorial.

	￼<!DOCTYPE html PUBLIC “-//W3C//DTD XHTML 1.0 Strict//EN” “http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd”>
	<html xmlns=”http://www.w3.org/1999/xhtml”>
		<head>
			<title>This is the Page Title</title>
			<link href=”styles.css” rel=”stylesheet” type=”text/css” media=”screen” />
		</head>
		<body>
			<div id=”container”>
				<div id=”header”>Header </div>
				<div id=”content”>Content</div>
				<div id=”sidebar”>Sidebar</div>
				<div id=”footer”>Footer</div>
			</div>
		</body>
	</html>

#### Summary
This has been a **VERY** quick overview of **XHTML** and its structure, hopefully however it will make the **index**. html template for the theme clearer. The next chapter will cover the basics of **CSS** and styling a webpage.

### CSS
**CSS** stands for **Cascading Style Sheets** and is widely used by all modern web designers to style webpages. It allows for an incredible level of flexibility to be applied to your site and once understood is very simple to use.

#### CSS Selectors
A **CSS** statement is formed in three parts, the **selector**, the **property** and a **value**.

	body { color: red; }

Here body is the **selector**, color the **attribute** and red the **value**. This command will style the color of all of the text on the page red. Simple.

A selector can have as many properties as you wish. These are wrapped in curly braces.

	￼p {
		color: blue;
		font-size: 20px;
		font-weight: bold;
	}

This statement styles all paragraph text blue, bold and has a font size of 20px. Properties end in a colon and values a semi-colon.

You may have noticed from the previous examples that **CSS** communicates with your **XHTML** content using the markup tags for example &lt;body&gt;, &lt;p&gt; or &lt;a&gt;.

#### Global Selectors
Any tag within the <body> of your document can be styled with **CSS**. For example.

	a { font-weight: bold; }

All of the anchor tags in your page will now be bold.

#### Class Selectors
We may want to select only specific parts of our webpage for styling. For example we may want certain paragraphs in out document to be a different colour to the main text.

We looked at the class attribute in the previous chapter, now can see how it can be used to select only specific tags. For example in our **XHTML** document we can enter;

	￼<p class=”important”>This paragraph is more important than the others.</p>

Using **CSS** we can then select all elements with the class=”important” attribute. Classes in **CSS** are preceded by a “.” (period).
	.important { color: red; }

#### ID Selectors
General and class selectors can apply to many tags within your document, the third type will select only one instance. This is the ID attribute again it was used in the previous chapter to define our page container, header, content, sidebar and footer.

	￼<div id=”container”>Page content will be inserted between these tags.</div>

**CSS** uses a # to identify **ID** attributes.

	#container {width: 800px;}

This will set the width of our page to 800px.

#### Nested Styles
When you look at the **styles.css** document you may notice that there are entries that have more than one selector. For example.

	#contentContainer #content {...}

This simply means that the the **CSS** should style the element with the **ID** of content inside the element with the **ID** of #contentContainer. This is a useful way of targeting elements without having to give every element of your website and individual **class** or **ID**.

Another example would be selecting all anchor elements &lt;a&gt; inside paragraphs &lt;p&gt; in the sidebar perhaps to make them a different colour from other anchors in the page.
	#sidebar p a {...}

#### Linking the styles.css file to index.html
In order for the browser to find our stylesheets we need to link the **styles.css** to the **index.html** file. This can be done with the &lt;link&gt; tags inserted in the document &lt;head&gt; if you look at the example in the previous chapter you will see the &lt;link&gt; after the &lt;title&gt; tag.

	￼<link href=”%pathto(styles.css)%” rel=”stylesheet” type=”text/css” media=”screen”  />

This link tells the browser where to locate the styles.css file and will load it accordingly.

#### Summary
Again this chapter has quickly outlined the basics of CSS and how it can be applied to a document, it may be worth your time creating an index.html file containing a basic site layout and linking it to a styles.css file. Then add some basic HTML to the page and try styling some tags, classes and ID's to get a feel of how it works.

The next chapter covers the RapidWeaver specific tags used by the program to generate the final webpages.

## Rapidweaver Templates

### The index.html file
The **index.html** file contained in the theme folder is the framework for all your other pages to be generated from. Open **index.html** in your text editor and you'll see that it is a standard **XHTML** page as described in the previous chapter but it also includes numerous RapidWeaver **Syntax Tags**.

### Document Structure
The themes **index.html** file follows a familiar structure that is common in nearly all modern webpages. This section aims to familiarise you with the template document.

The basic layout of the page should by now be familiar;

	<!DOCTYPE html PUBLIC “-//W3C//DTD XHTML 1.0 Strict//EN” “http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd”>
	<html xmlns=”http://www.w3.org/1999/xhtml”>
		<head>
			<title>This is the Page Title</title>
			<link href=”styles.css” rel=”stylesheet” type=”text/css” media=”screen” />
		</head>
		<body>
			<div id=”container”>
				<div id=”pageHeader”>
					<h1>%site_title%</h1>
					<h2>%site_slogan%</h2>
				</div>
				<div id=”contentContainer”>
					<div id=”content”>
						Content
					</div>
				</div>
				<div id=”sidebarContainer”>
					<div id=”navcontainer”>
						%toolbar%
					</div>
					<div id=”sidebar”>
						%sidebar%
					</div>
				</div>
				<div id=”footer”>Footer</div>
			</div>
		</body>
	</html>

The main content areas are distinguished by &lt;div&gt; elements, each open and close tag contains a **Syntax Tag**. For example.

	<div id=”content”>%content%</div>

The majority of the syntax tags relate directly back to a text area in RapidWeaver, it should be pretty obvious which tag corresponds to which area but there is a definition list in the **RapidWeaver Theme Syntax** chapter located in the appendix at the end of this document[[1]][fn1].

[fn1]: <#fn1> (Footnote 1)

We have tried to comment **index.html** document in the **tutorial.rwtheme** file to make it as clear as possible where your content is inserted by RapidWeaver.
## Footnotes
1. <a name="fn1"></a>Some tags like the %plugin_sidebar% are there for code to be entered by page plugins such as the blog and thus have no user text input.