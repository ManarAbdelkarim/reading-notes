
# Chapter 5: “Images”
## How to add Images?

1. use <img\>  tag

2. use **src** attribute which is the path or link to an image ,

optional Attributes:

1. **alt :** attribute tells what is the image about .
2. **title :** You can also use the title attribute with the <img\>element to provide additional information about the image.

Example:

          <img src="img/teamAttack.jpg" alt="Attack On Titans" title="Attack On Titans"/> 

The Result:

 <img src="img/teamAttack.jpg" alt="Attack On Titans" title="Attack On Titans"/> 

## Rules for Creating Images:

1. Save images in the right format

2. Save images at the right size

3. Use the correct resolution

## which image format should you use ?
- JPEG : Whenever you have many different colors in a picture
-  GIF or PNG : when saving images with few colors or large areas of the same color.

![jpeg vs jpg vs png](https://img.pagecloud.com/wAegMZSQrxtIBtV-i7jBCW-Ho7Y=/1000x0/filters:no_upscale()/blogmerge/cf67f56e-00e6-48c0-a1a4-31a8e3baf0de.jpeg)

### The effect on images :

![jpeg vs jpg vs png](https://img.pagecloud.com/z5uzgd5WtahuFVPgBQKVscqeytA=/1000x0/filters:no_upscale()/blogmerge/7787ce0e-0c64-4c4f-b285-8b4dbc9e21ef.jpeg)

# Chapter 11: “Color” 

The color property allows you to specify the color of text inside an element.

## How to specify a color ?

1. **rgb values :** These express colors in terms of how much red, green and blue are used to make it up.

For example: rgb(209, 0, 0)

        <p style="color:rgb(209, 0, 0)">Hello World</p>

 <p style="color:rgb(209, 0, 0)">Hello World</p>

 2. **hex codes :** These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign.
 
  For example: #6495ED

        <p style="color :#6495ED">Hello World</p>

 <p style="color : #6495ED">Hello World</p>

 3. **color names :** There are 147 predefined color names that are recognized by browsers.
 
  For example: DeepPink.


        <p style="color:DeepPink">Hello World</p>

<p style="color:DeepPink">Hello World</p>

## CSS Fonts :

The CSS font properties define the font family, boldness, size, and the style of a text.

**Difference Between Serif and Sans-serif Fonts:**

![Difference Between Serif and Sans-serif Fonts](https://www.w3schools.com/css/serif.gif)

# Chapter 12: “Text”

## Text in css:

- ### font-family
The font-family CSS property specifies a prioritized list of one or more font family names and/or generic family names for the selected element.

For Example:

     font-family: Georgia, serif;

<p style="font-family: Georgia, serif;">Hello World</p>
- ### font-size
The font-size CSS property sets the size of the font. Changing the font size also updates the sizes of the font size-relative <length\> units, such as em, ex, and so forth.

For Example:

        font-size: 1.2em;

<p style="font-size: 1.2em;">Hello World</p>


- ### @font-face
The @font-face CSS at-rule specifies a custom font with which to display text; the font can be loaded from either a remote server or a locally-installed font on the user's own computer.

For Example:

            @font-face {
            font-family: "Open Sans";
            src: url("/fonts/OpenSans-Regular-webfont.woff2")
             format("woff2"),
            url("/fonts/OpenSans-Regular-webfont.woff") format("woff");
                  }


- ### font-weight
The font-weight CSS property sets the weight (or boldness) of the font. The weights available depend on the font-family that is currently set.

For Example:

            font-weight: bold;

<p style="font-weight: bold;">Hello World</p>

- ### font-style
The font-style CSS property sets whether a font should be styled with a normal, italic, or oblique face from its font-family.

For Example:

       font-style: italic;

<p style="font-style: italic;">Hello World</p>

- ### text-transform
The text-transform CSS property specifies how to capitalize an element's text. It can be used to make text appear in all-uppercase or all-lowercase, or with each word capitalized.

For Example:

         text-transform: capitalize;

<p style="text-transform: capitalize;">Hello World</p>

- ### text-decoration
The text-decoration shorthand CSS property sets the appearance of decorative lines on text. 


For Example:

          text-decoration: underline dotted red;

<p style="text-decoration: underline dotted red;">Hello World</p>

- ### line-height
The line-height CSS property sets the height of a line box. It's commonly used to set the distance between lines of text. On block-level elements, it specifies the minimum height of line boxes within the element.

For Example:

        line-height: 32px;

<p style="line-height: 32px;">Hello World</p>

- ### letter-spacing, 
The letter-spacing CSS property sets the horizontal spacing behavior between text characters.

For Example:

        letter-spacing: 1px;

<p style="letter-spacing: 1px;">Hello World</p>

- ### word-spacing
The word-spacing CSS property sets the length of space between words and between tags.

For Example:

        word-spacing: 1rem;

<p style="word-spacing: 1rem;">Hello World</p>

- ### text-align
The text-align CSS property sets the horizontal alignment of a block element or table-cell box. This means it works like vertical-align but in the horizontal direction.

For Example:

        text-align: left;

<p style="text-align: left;">Hello World</p>

- ### vertical-align
The vertical-align CSS property sets vertical alignment of an inline, inline-block or table-cell box.


For Example:

        vertical-align: top;

<p style="vertical-align: top;">Hello World</p>

- ### text-indent
The text-indent CSS property sets the length of empty space (indentation) that is put before lines of text in a block.

For Example:

        text-indent: 30%;

<p style="text-indent: 30%;">Hello World</p>

- ### text-shadow
The text-shadow CSS property adds shadows to text. It accepts a comma-separated list of shadows to be applied to the text and any of its decorations. 


For Example:

     text-shadow: red 2px 5px;

<p style="text-shadow: red 2px 5px;">Hello World</p>

- ### :first-letter, :
The ::first-letter CSS pseudo-element applies styles to the first letter of the first line of a block-level element, but only when not preceded by other content 


For Example:

        p::first-letter {
        font-size: 130%;
            }



- ### first-line
The ::first-line CSS pseudo-element applies styles to the first line of a block-level element.

For Example:

        p::first-line {
          color: red;
        }




- ### :link, :visited


- ### Responding to Users :hover, :active, :focus