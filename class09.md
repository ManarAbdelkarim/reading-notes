# Read: 09 - Forms and Events

## Chapter 7: “Forms” 
### What is form?
Forms are used to collect the user input details and process it via servers.Most of the websites use the login form to collect users informationThe best known form on the web is probably the search box that sits right in the middle of Google's homepage
In addition to enabling users to search, forms also allow users to perform other functions online. You will see forms when registering as a member of a website, when shopping online, and when signing up for newsletters or mailing lists.

![](https://upload.wikimedia.org/wikipedia/commons/3/34/Sample_web_form.png)

- <label\> tag in HTML
This is optional tag in HTML form. It is simply the view or label name for the input tag.
- <input\> tag in HTML
This tag is where the user needs to send the input of the form.
- Radio Button
It gives an option where we can select any one button out of many options.

e.i:

     <form>

     <input type="radio" name="status" value="Married" checked> Married<br>

     <input type="radio" name="status" value="Single"> Single<br>

     <input type="radio" name="status" value="Widow"> Widow 

     </form>

<form>

<input type="radio" name="status" value="Married" checked> Married<br>

<input type="radio" name="status" value="Single"> Single<br>

<input type="radio" name="status" value="Widow"> Widow 

</form>

- Text Input
It defines: a Single-line input field for text input.

       <form> 
       First Name: <input type="text" name="firstname">
       <br> 
       <br>
       Last Name: <input type="text" name="lastname">

       </form> 

<form> 
First Name: <input type="text" name="firstname">
<br> 
<br>
Last Name: <input type="text" name="lastname">

</form> 

<br><br>
- Submit Button: 
The submit button submits the form.



       <form action="Form.php" method="post">
       First Name:<br>
       <input type="text" name="fname">
       <br>
       Last Name<br>
       <input type="text" name="lname">
       <br><br>
       <input type="submit">
       </form>

       <!DOCTYPE html>
<html>
<body>

<h2>Example for Submit Button</h2>
<form action="Form.php" method="post">
First Name:<br>
<input type="text" name="fname">
<br>
Last Name<br>
<input type="text" name="lname">
<br><br>
<input type="submit">
</form>

</body>
</html>


- There are several types of form controls that you can use to collect information from visitors
to your site.
ADDING TEXT,
Making Choices,
Submitting Forms, Uploading Files,

- Password input
like a single line text box but it
masks the characters entered.
Text input (single-line)
Used for a single line of text such
as email addresses and names.

- Text area (multi-line)
For longer areas of text, such as
messages and comments.

- visitors you will need a form, which lives inside a element.
- Information from a form is sent in name\value pairs.
- Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.
- HTML5 introduces new form elements which make it easier for visitors to fill in forms.
- List markers can be given different appearances using the list-style-type and list-style image properties.
- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.
- Forms are easier to use if the form controls are vertically aligned using CSS.
- Forms benefit from styles that make them feel more interactive.


## summary:
- Whenever you want to collect information from visitors you will need a form, which lives inside a <form\> element.

- Information from a form is sent in name/value pairs.

- Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

- HTML5 introduces new form elements which make it easier for visitors to fill in forms.

## Chapter 14: “Lists, Tables & Forms”

### Table:
The HTML <table\> element represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns of cells containing data.

### tbody:
The HTML Table Body element (<tbody\>) encapsulates a set of table rows (<tr\> elements), indicating that they comprise the body of the table (<table\>).

### tfoot :
The HTML <tfoot\> element defines a set of rows summarizing the columns of the table.

### thead:
The HTML <thead\> element defines a set of rows defining the head of the columns of the table.

### tr :
The HTML <tr\> element defines a row of cells in a table. The row's cells can then be established using a mix of <td\> (data cell) and <th\> (header cell) elements.

### td:
The HTML <td\> element defines a cell of a table that contains data. It participates in the table model.


     <html>
      
       <head>
      
       <style>
      
       table,
      
       td {
      
           border: 1px solid #333;
       }
      
       thead,
      
       tfoot {
      
           background-color: #333;
      
           color: #fff;
       }
      
       </style>
      
       </head>
      
       <table>
      
           <thead>
      
               <tr>
      
                   <th colspan="2">The table header</th>
      
               </tr>
      
           </thead>
      
           <tbody>
      
               <tr>
      
                   <td>The table body</td>
      
                   <td>with two columns</td>
      
               </tr>
      
           </tbody>
      
       </table>
      
       </html>





<html>
<head>
<style>
table,
td {
    border: 1px solid #333;
}

thead,
tfoot {
    background-color: #333;
    color: #fff;
}
</style>
</head>
<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>
</html>


## Events:

## what are Events?

![](data:image/jpeg;base64,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)

DIFFERENT EVENT TYPES Here is a selection of the events that occur in the browser while you are browsing the web. Any of these events can be used to trigger a function in your JavaScript code. UIEVENTS Occur when a user interacts with the browser's user interface (UI) rather than the web page

![](https://cope-ali.github.io/cope-ali261.github.io/img/HTMLevents.png)

- Events are the browser's way of indicating when something has happened (such as when a page has finished loading or a button has been clicked).
- Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.
- When an event occurs on an element, it can trigger a JavaScript function.
- When this function then changes the web page in some way, it feels interactive because it has responded to the user.
- You can use event delegation to monitor for events that happen on all of the children of an element.
- The most commonly used events are W3C DOM events, although there are others in the HTMLS specification as well as browser-specific events.

