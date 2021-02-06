# HTML

## *Chapter 1: "Structure"*

 HTML pages are text documents that composed of three main parts:
1. a line containing HTML version information.

2.  declarative header section (delimited by the HEAD element)

3.  body, which contains the document's actual content. 


![html](https://www.jaimebutler.ch/jb-edit/wp-content/uploads/2014/07/Basic-HTML.png)

## Tags (Elements):
adding tags or elements to the words will give the information they surround special
meaning so that the browser knows what is
a heading, where a paragraph begins and ends, and so on.
HTML elements are these characters that live inside angled
brackets. Each HTML element tells the browser something about the information that sits between its tags.

 Elements are usually made up of two tags: 

*  opening tag and : <element\>
*  closing tag. (The closing tag has an extra forward slash in it.) : </element\>

There are two different types of tags:-> 
* Container Element: -> Container Tags contains start tag & end tag i.e.
 \
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<HTML\>.<\/HTML>
*  Empty Element:-> Empty Tags contains start tag i.e.
\
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <br\>

## Attributes 
&nbsp; Attributes provide additional informationabout the contents of an element. They appear on the opening tag of the element and are made up of two parts:
 * name : specifies a name for an HTML element, indicates what kind of extra information you are supplying about the element's content. It should be
written in lowercase.

 * value: specifies the value of an <input\> element,iit is the information
or setting for the attribute. It should be placed in double quotes.

 ![attribue](https://www.computerhope.com/jargon/h/html-tag.gif)


## Summary
STRUCTURE
* HTML pages are text documents.
* HTML uses tags (characters that sit inside angled
brackets) to give the information they surround special
meaning.
* Tags are often referred to as elements.
* Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.
* Opening tags can carry attributes, which tell us more
about the content of that element.
* Attributes require a name and a value.
* To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go.


## *Chapter 8: “Extra Markup”*


## DOCTYPES:
It is an "information" to the browser about what document type to expect.Each web page should begin with DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included).
* HTML 5:

< !DOCTYPE html\>
* XML:

< ?xml version="1.0"?\>

## Comments:


If you want to add a comment to your code that will not be visible in the user's browser, comments help to understand the code for you in future or to other developers. to type a comment you can add the text between these characters:

<\!-- comment goes here -->

## ID Attribute:
The id attribute specifies a unique id for an HTML element. It is used to
uniquely identify that element from other elements on the page. The id attribute is known as a ***global attribute*** because it can be used on any element.

<element id="special-id-name"\>

## Class Attribute:
 the Class Attribute specify a class for an HTML element. Multiple HTML elements can share the same class rather than uniquely identifying one element within a document.

<element class="class-name"\>

## Block Elements:
block level elements are elements that will always
appear to start on a new line in
the browser window. i.e :
\
\
<article\>
<aside\>
<dd\> <div\>
\
\
<dl\><dt\><footer\><form\>
\
\
<h1\>-<h6\><header\><hr\>
\
\
<li\><main\><nav\><ol\><p\>
\
\
<section\><table\><ul\><video\>

## Inline Elements:
 Inline Elements are elements that will always appear to continue on the
same line as their neighbouring elements. An inline element does not start on a new line. i.e:
\
\
<a\><br\><button\><em\>
\
\
<i\><img\><input\><label\>
\
\
<script\><select\><span\><tt\>
\
\
<strong\><textarea\><time\>


An inline element only takes up as much width as necessary. 

![block and inline](https://data-flair.training/blogs/wp-content/uploads/sites/2/2020/06/Block-level-Inline-elements-in-html-df.jpg)


## Grouping Text & Elements In a Block:
* **<div\>**

 The <div\> element allows you to group a set of elements together in one block-level box.

## Grouping Text & Elements Inline:

* **<span\>**

The <span> element acts like
an inline equivalent of the <div\>
element. It is used to either:

 1. Contain a section of text where there is no other suitable element to differentiate it from its surrounding text.
 2. Contain a number of inline elements.

 ![div vs span](https://disenowebakus.net/en/images/articles/div-block-span-inline.jpg)

## IFrames:

An iframe is like a little window that has been cut into your page — and in that window you can see another page. The term iframe is an abbreviation of inline
frame.

An iframe is created using the
<iframe\> element. There are a
few attributes that you will need
to know to use it:

* src

The src attribute specifies the URL of the page to show in the frame.

* height

The height attribute specifies the height of the iframe in pixels.

* width

The width attribute specifies the width of the iframe in pixels.

* seamless

seamless can be applied to an iframe where scrollbars are not desired
\
\
Example :

> < iframe width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed"\>
</iframe\>

The Result:
<iframe
width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed">
</iframe>


## Information About Your Pages:

##  What is *<meta\>*:

The <meta\> element lives inside the <head\> element and contains information about that web page.

## Meta Attributes:

* **charset:** Specifies the character encoding for the HTML document

* **content:** Specifies the value associated with the http-equiv or name attribute

* **http-equiv:** Provides an HTTP header for the information/value of the content attribute

* **name:** Specifies a name for the metadata.

   Name Values:
	* application-name
    * author
    * description
    * generator
    * keywords
    * viewport	



## Summary
EXTRA MARKUP
* DOCTYPES tell browsers which version of HTML you
are using.
* You can add comments to your code between the
<\!-- and --> markers.
* The id and class attributes allow you to identify
particular elements.
* The <div\> and <span\> elements allow you to group
block-level and inline elements together.
* <iframes\> cut windows into your web pages through
which other pages can be displayed.
* The <meta\> tag allows you to supply all kinds of
information about your web page.
* Escape characters are used to include special
characters in your pages such as <, >, and ©.



## *Chapter 17: "HTML5 Layout"*


## Traditional HTML Layouts:
authors used <div\> elements to group
together related elements on the page then  used class or id attributes
to indicate the role of the <div\> element in the structure of the page.
![Traditional layout](https://csharpcorner.azureedge.net/UploadFile/b5be7f/working-with-new-semantic-elements-in-html5-along-with-html/Images/Html%20Basic%20Structure%20Image.png)


## New Html5 Layout Elements:

HTML5 introduces a new set of elements that allow you to divide up the
parts of a page. The names of these elements indicate the kind of content
you will find in them.

![html5 layout](https://mobile.developer.com/imagesvr_ce/3977/Figure01.png)


## Headers & Footers (<header\> <footer\>):

A header or footer for an individual <article\> or <section\> within the page.
e <header\> element used to contain the site name and the main navigation.
The <footer\> element contains copyright information, along
with links to the privacy policy and terms and conditions. 


## Navigation (<nav\>):
The <nav\> element is used to contain the major navigational
blocks on the site such as the primary site navigation.

## Articles (<article\>):
The <article\> element acts asa container for any section of apage that could stand alone and potentially be syndicated.

## Asides (<aside\>):
The <aside\> element has two purposes, depending on whether it is inside an <article\> element or not


## Sections (<section\>):

The <section\> element groups related content together, and
typically each section would have its own heading.

## Heading Groups (<hgroup\>):
The purpose of the <hgroup\>element is to group together a set of one or more <h1\> through <h6\> elements so that they are treated as one single heading


## Figures(<figure\> <figcaption\>)

 <figure\> can be used to contain any content that is
referenced from the main flow of an article (not just images).


## Summary
HTML5 LAYOUT
*  The new HTML5 elements indicate the purpose of
different parts of a web page and help to describe
its structure.
* The new elements provide clearer code (compared
with using multiple <div> elements).
* Older browsers that do not understand HTML5
elements need to be told which elements are
block-level elements.
* To make HTML5 elements work in Internet Explorer 8
(and older versions of IE), extra JavaScript is needed,
which is available free from Google.



 ## *Chapter 18: "Process & Design"*
 ## wireframe :
 
 wireframe is a simple sketch of the key information that needs to go on each page of a site. Wireframes allow you to organize the information that will need to go on each page.

![wireframe](https://www.freepik.com/blog/app/uploads/2019/05/how-use-wireframes-web-design-Cover-post-100.jpg)


## site map:
A site map is a tool used to help keep you and your site organized. Site maps are like a family trees consisting of pages instead of relatives, that lead to information from one page to the next and back.

![site map](https://creativepublic.com/assets/sitemap_structure.gif)

 ## Summary
PROCESS & Design
* It's important to understand who your target audience
is, why they would come to your site, what information
they want to find and when they are likely to return.
* Site maps allow you to plan the structure of a site.
* Wireframes allow you to organize the information that
will need to go on each page.
* Design is about communication. Visual hierarchy helps
visitors understand what you are trying to tell them.
* You can differentiate between pieces of information
using size, color, and style.
* You can use grouping and similarity to help simplify
the information you present.