# Domain Modeling

## what is Domain Modeling?
Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.(Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that’s articulated well can verify and validate your understanding of that problem.)

![domain](https://lh3.googleusercontent.com/proxy/xWpzhH4APZdTPOAjelHa8HsGCe6f6SkLXZa2QoMuJDp8k8665Lr1ut7VgaFD-3WL_e1wXZJUB_Zbdfe3KrYdUE7AJs4ioWkzSnpjdtnQ93ok)



# Chapter 6: “Tables”

### what do we mean by tables?

A table reprsents inforrmation in a grid format, and grids can help us understand complex data by referencing the information on two axes.
The table elemebt is used to create a table and we use tr for each new row and we use td for each cell in that row .we use th for the table heading and you can expand the column by adding colspan attr to th or td . and you can extend a row by the rowspan attr added to the th or td . you can use thead and tbody and tforr for long tables to distinguish it .

![tables](https://static.javatpoint.com/htmlpages/images/html-table-width.png) 

### Table Structure:

- <table\> element represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns of cells containing data.
- <tbody\>encapsulates a set of table rows (<tr> elements), indicating that they comprise the body of the table (<table>).
- <td\> element defines a cell of a table that contains data. It participates in the table model.
- <thead\> element defines a set of rows defining the head of the columns of the table.
- <tfoot\> element defines a set of rows summarizing the columns of the table.



       <table>
           <thead>
               <tr>
                   <th>Items</th>
                   <th scope="col">Expenditure</th>
               </tr>
           </thead>
           <tbody>
               <tr>
                   <th scope="row">Donuts</th>
                   <td>3,000</td>
               </tr>
               <tr>
                   <th scope="row">Stationery</th>
                   <td>18,000</td>
               </tr>
           </tbody>
           <tfoot>
               <tr>
                   <th scope="row">Totals</th>
                   <td>21,000</td>
               </tr>
           </tfoot>
       </table>

output:

<table>
    <thead>
        <tr>
            <th>Items</th>
            <th scope="col">Expenditure</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Donuts</th>
            <td>3,000</td>
        </tr>
        <tr>
            <th scope="row">Stationery</th>
            <td>18,000</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th scope="row">Totals</th>
            <td>21,000</td>
        </tr>
    </tfoot>
</table>

# Chapter 3: “Functions, Methods, and Objects"

## what is the object?
The Object class represents one of JavaScript's data types. It is used to store various keyed collections and more complex entities.
The new keyword and the object constructor create a blank object, you can then add properties and methods to the object.
## WAYS TO CREATE OBJECT:
1.  Object literals using { }
2. Object literals using { key : value }
3. Using new Object()
4. Using Object.create()
5. Using function constructor
6. Using anonymous function
7. Using ES6 class keyword


![ways](https://lh3.googleusercontent.com/proxy/yzH-YrgXVCfmvMeh8PJh6IDm89iaM5lb-wfoBGLTFB8qZa48aZKlnVN9gZNR12wYZ2hlra9pCqiimwdidpCeq3_xU7hkyRauQtEJ-MqYn3B23FmrmZwk0GR9Sw-v4A)

## CONSTRUCTOR NOTATION:
Object constructors can use a function as a template for creating objects. First, create the template with the object’s properties and methods. A function called Hotel will be used as a template for creating new objects that represent hotels. Like all functions, it contains statements. In this case, they add properties or methods to the object. The function has three parameters.

e,i:
            class Polygon {
          constructor() {
            this.name = 'Polygon';
          }
        }

        const poly1 = new Polygon();

        console.log(poly1.name);


output:"Polygon"
