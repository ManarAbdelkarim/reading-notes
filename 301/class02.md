# PAIR PROGRAMMING


## JQuery

![JQuery](https://www.magesolution.com/blog/wp-content/uploads/2014/01/what-is-jquery-11.png)
### What is jQuery?

jQuery is a JavaScript file that you include in your web pages. 
It lets you find elements using CSS-style selectors and then do 
something with the elements using jQuery methods. 

#### 1: FIND ELEMENTS using JQuery:
  FIND ELEMENTS USING Css-STYLE SELECTORS by A function called jQuery
   () lets you find one or more elements in the page.

- SIMILARITIES TO DOM:

    -  jQuery selectors perform a similar task to traditional DOM queries, but the syntax is much simpler. 
     - You can store the jQuery object in a variable, just as you can with DOM nodes. 
     - You can use jQuery methods and properties (like DOM methods and properties) to manipulate the DOM nodes that you select.


####  2: DO SOMETHING WITH THE ELEMENTS USING JQUERY METHODS:

-  KEY DIFFERENCES FROM DOM:
    - It's cross-browser, and there's no need to write fallback code. 
    - Selecting elements is simpler (because it uses CSS-style syntax) and is more accurate.
    - Event handling is simpler as it uses one method that works in all major browsers. Methods affect all the selected elements without the need to loop through each one  
    - Additional methods are provided for popular required tasks such as animation 
    - Once you have made a selection, you can apply multiple methods to it.

    ### WHY USE JQUERY?

    ![WHY USE JQUERY](https://wptips.dev/wp-content/uploads/2021/01/thumb-use-jquery.jpg)

    jQuery doesn't do anything you cannot achieve with pure JavaScript.
    It is just a JavaScript file but estimates show it has been used on over a
    quarter of the sites on the web, because it makes coding simpler. 

    jQuery's motto is "Write less, do more," because it allows you to achieve
    the same goals but in fewer lines of code than you would need to write
    with plain JavaScript. 

    1. SIMPLE SELECTORS 

    2. COMMON TASKS IN LESS CODE 

    3. CROSS-BROWSER COMPATIBILITY 

-----------

## 6 Reasons for Pair Programming

![](https://i1.wp.com/blexin.com/wp-content/uploads/2020/12/01-1.png?fit=1024%2C608&ssl=1)


### How does pair programming work?
 pair programming commonly involves two roles:
 1. the Driver 
    - The Driver is the programmer who is typing and the only one whose hands are on the keyboard.
    - Handling the “mechanics” of coding, the Driver manages the text editor, switching files, version control, and—of course writing—code.
    - The Navigator uses their words to guide the Driver but does not provide any direct input to the computer.

 2.  the Navigator.
     -  The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs.
     - The Navigator might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

     ![](https://miro.medium.com/max/7676/1*sBJhFwmpfbftanqzxOeK_w.jpeg)
--------

### Why pair program?
1. Greater efficiency

    when two people focus on the same code base, it is easier to catch mistakes

2. Engaged collaboration

    When developers pair program, they rely more on each other and can often find a solution together 

3. Learning from fellow students

    working with a teammate can expose developers to techniques they otherwise would not have thought of. 

4. Social skills

    Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. 

5. Job interview readiness

    A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together

6. Work environment readiness

    Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product.

---------

## EFFECTS 

### BASIC EFFECTS 
                                  
METHOD                                 |                             DESCRIPTION                                |
| :-----------------------------------------------------------------------: | :-----------------------------------------------------------: |
|   . show ()  |  Displays selected elements|
|   . Hides () |  Hides selected elements|
|   . togg1e ()  |Toggles between showing and hiding selected elements|

### FADING EFFECTS

METHOD                                 |                             DESCRIPTION                                |
| :-----------------------------------------------------------------------: | :-----------------------------------------------------------: |
|   . fadeln ()  |  Fades in selected elements making them opaque|
|   . fadeout () |Fades out selected elements making them transparent|
|   . fadeTo ()  |Changes opacity of selected elements|
|   .fadeTogg1e()  |Hides or shows selected elements by changing theiropacity (the opposite of their current state)|




### SLIDING EFFECTS
METHOD                                 |                             DESCRIPTION                                |
| :-----------------------------------------------------------------------: | :-----------------------------------------------------------: |
|   . slideUp ()  |  Shows selected elements with a sliding motion|
|   . slideDown () |  Hides selected elements with a sliding motion|
|   .s1ideToggle()  |Hides or shows selected elements with a sliding
motion (in the opposite direction to its current state)|


### CUSTOM EFFECTS

METHOD                                 |                             DESCRIPTION                                |
| :-----------------------------------------------------------------------: | :-----------------------------------------------------------: |
|   . delay ()  |  Delays execution of subsequent items in queue|
|   . stop () |  Stops an animation if it is currently running|
|   .animate()  |Creates custom animations|

-------------

## FINDING ELEMENTS (Using JQuery)

### CONTENT FILTERS

##### **GET/ CHANGE CONTENT:**
 - .html()
 - .replaceWith() 
 - .text()
 - .remove() 

##### **ELEMENTS:**
 - . before()
 - .after()
 - .prepend() 
 - .append()
 -  .remove() 
 - .clone()
 - .detach()
 - .empty()
 - .add() 

#### **ATTRIBUTES:**

- .attr () 
- .removeAttr ()
- .addClass() 
- .removeClass()
- .css()

#### **FORM VALUES:**

- . val() 
- . i sNumeric () 
GENERAL
- .text() 
- .closest() 
-  . parent()
-   .parents() 
- .children() 
- .siblings() 
-  .next() 
- . nextAll () 
- .prev() 
- . prevAll () 