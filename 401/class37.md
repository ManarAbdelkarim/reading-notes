# React 1

## Why JSX?
React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

## How Does JSX Work?

When the JSX expressions are compiled, they are converted into JavaScript objects, representing React elements.
React then uses these elements to build the corresponding HTML DOM and display it in the browser.

Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.

## Rendering Elements

use  ReactDOM.render()

    <div id="root"></div>
    const element = <h1>Hello, world</h1>;
    ReactDOM.render(element, document.getElementById('root'));

## Updating the Rendered Element

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().

### `NOTE: React Only Updates What’s Necessary`

## Function and Class Components

- function component :

        function Welcome(props) {
        return <h1>Hello, {props.name}</h1>;
        }
    
- class component :

        class Welcome extends React.Component {
        render() {
            return <h1>Hello, {this.props.name}</h1>;
        }
        }

### `Note: Props are Read-Only`


## State:
Many web apps need their components to change their data, for example, after user interaction (clicking a button, submitting a form, etc.).
However, props cannot be changed.

In order to allow components to manage and change their data, React provides a feature called state.
State is an object that is added as a property in class components.

## Changing State

State should not be modified directly. Instead, React provides a setState() method, that can be used to modify state.

## lifecycle methods

React provides special lifecycle methods for class components, which are called when components are mounted, updated or unmounted.

- Mounting is the process when a component is rendered on the page.
- Unmounting is the process when a component is removed from the page.

- The componentDidMount method is called when a component is rendered on the page.

- Another lifecycle method is componentDidUpdate(), which is called when a component is updated in the DOM.

- Another lifecycle method is componentWillUnmount(), which is called when a component is remove in the DOM 

## The useEffect Hook


- The lifecycle methods we covered are only available for class components.

- React provides a special Hook called useEffect to make lifecycle methods available in functional components. It combines the componentDidMount, componentDidUpdate, and componentWillUnmount methods into one.

## Handling Events

Handling events in React is very similar to handling events in the DOM.

The only difference is that event names use camelCase syntax and the event handler needs to be passed in curly braces.

## Handling User Input

One of the common ways that users interact with web pages is through text fields.

We can handle user input in React using the onChange event of the text field.
When the value of the text field changes, the event handler is called, updating the value of the field in the component's state.
This way you always have the actual value of the text field in the state.