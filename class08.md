# Chapter 15, “Layout”

HTML5 introduces a new set of elements that allow you to divide up the
parts of a page. The names of these elements indicate the kind of content
you will find in them.

- css is how you control the looks of your **html** .
- The element inside other elemnents are called child element and the outer element is the parent .
- In normal flow, each block-level element sits on top of the next
one. Since this is the default
way in which browsers treat
HTML elements, you do not
need a CSS property to indicate
that elements should appear
in normal flow.
- You then use the offset 
properties (top or bottom and
left or right) to indicate how
far to move the element from
where it would have been in
normal flow.

![html5 layout](https://mobile.developer.com/imagesvr_ce/3977/Figure01.png)


## Containing Elements

**Key Concepts in Positioning Elements :**

If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

- Building Blocks
CSS treats each HTML element as if it lives in its own box (we have a tactile demonstration). You can set several properties that affect the appearance/dimensions of these boxes.

The properties of the box we can control with CSS are element margins, and padding for each box with CSS. Here is a breakdown of what each means:

- **Border** - Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.
- **Margin** - Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.
- **Padding** - Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.

![boxes](https://thecustomizewindows.com/wp-content/uploads/2015/05/figure-vs-img-Tag-in-HMTL5-WordPress-Posts.png)

* Containing Elements
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
![Containing](https://www.learnpick.in/userfiles/resources_conversion_files/presentation_html_1496646237_82537-10.jpg)

* Controlling the Position of Elements

-CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning.
![position](Images/10.png)
### Floating Elements

 #### ***What is Float ?***

Floating an element changes the behavior of that element and the block level elements that follow it in normal flow. The element is moved to the left or right and removed from normal flow, and the surrounding content floats around the floated item.

 The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.

 -To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed.

<h3 style="color:red;">Note:</h3>
The floated element becomes a block-level element around which other
content can flow.

#### ***The float property values:***

- left 
- right 
- none 
- inherit  


## Positioning :

#### ***What does Positioning do?***


Positioning allows you to move an element from where it would be placed when in normal flow to another location. Positioning isn’t a method for creating your main page layouts

- Normal flow :
is the way that Block and Inline elements are displayed on a page before any changes are made to their layout.

        position:static

- Relative Positioning 
Relative positioning moves an element in relation to where it would have been in normal flow.


        
        position:relative

- Absolute Positioning 
When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page.

     
        position:absolute

- Fixed Positioning 
Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.


        position:fixed

## Screen Resolution
Resolution refers to the number of dots a screen shows per inch. Some
devices have a higher resolution than desktop computers and most
operating systems allow users to adjust the resolution of their screens.

![Screen Resolution](./img/Resolutions.png)

## Liquid Layouts
Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.

![Liquid](https://helpx.adobe.com/content/dam/help/en/indesign/using/alternate-layouts-liquid-layouts/_jcr_content/main-pars/image/adaptive_layout_workflow.png)

## Layout Grids
Composition in any visual art (such as design, painting, or photography) is the placement or arrangement of visual elements. Grids help create professional and flexible designs You can include multiple CSS files in one page.

Conclusion :
- the <div\> elements are often used as containing elements to group together sections of a page.
- Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.
- The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)
- Pages can be fixed width or liquid (stretchy) layouts.
- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).
- Grids help create professional and flexible designs.
- CSS Frameworks provide rules for common tasks.
- You can include multiple CSS files in one page.