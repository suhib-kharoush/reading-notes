# Conditional Rendering

- Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

- Consider these two components:

`function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}`


Create a Greeting component that displays either of these components depending on whether a user is logged in:

`function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}`

`ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,
  document.getElementById('root')
);`


##### Element Variables
- Consider these two new components representing Logout and Login buttons:

`function LoginButton(props) {
  return (
    <button onClick={props.onClick}>
      Login
    </button>
  );
}

function LogoutButton(props) {
  return (
    <button onClick={props.onClick}>
      Logout
    </button>
  );
}`


##### Inline If with Logical && Operator
- You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator. It can be handy for conditionally including an element:

`function Mailbox(props) {
  const unreadMessages = props.unreadMessages;
  return (
    <div>
      <h1>Hello!</h1>
      {unreadMessages.length > 0 &&
        <h2>
          You have {unreadMessages.length} unread messages.
        </h2>
      }
    </div>
  );
}`

`const messages = ['React', 'Re: React', 'Re:Re: React'];
ReactDOM.render(
  <Mailbox unreadMessages={messages} />,
  document.getElementById('root')
);
`

##### Inline If-Else with Conditional Operator
- Another method for conditionally rendering elements inline is to use the JavaScript conditional operator `condition ? true : false`.

- In the example below, we use it to conditionally render a small block of text.

``render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
      The user is <b>{isLoggedIn ? 'currently' : 'not'}</b> logged in.
    </div>
  );
}``

- It can also be used for larger expressions although it is less obvious what’s going on:

```render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
      {isLoggedIn
        ? <LogoutButton onClick={this.handleLogoutClick} />
        : <LoginButton onClick={this.handleLoginClick} />
      }
    </div>
  );
}
```

##### Preventing Component from Rendering
- In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return `null` instead of its render output.



# List and Keys

- Given the code below, we use the `map()` function to take an array of numbers and double their values. We assign the new array returned by `map()` to the variable doubled and log it:
``const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);``

- This code logs [2, 4, 6, 8, 10] to the console.

##### Rendering Multiple Components

 -We can build collections of elements and `include them in JSX` using curly braces `{}`.

##### Basic List Component

- We can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.

``function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li>{number}</li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);``

- When we run this code, you’ll be given a warning that a key should be provided for list items. A “key” is a special string attribute you need to include when creating lists of elements. We’ll discuss why it’s important in the next section.

##### Keys

- Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity:


``const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);``

- The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys:
``const todoItems = todos.map((todo) =>
  <li key={todo.id}>
    {todo.text}
  </li>
);``


# Forms

- HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state. For example, this form in plain HTML accepts a single name:


``<form>
  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>``

- This form has the default HTML form behavior of browsing to a new page when the user submits the form.

##### Controlled Components

- In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with `setState()`.

##### The textarea Tag
- In HTML, a `<textarea>` element defines its text by its children:
``
<textarea>
  Hello there, this is some text in a text area
</textarea>
``

##### The file input Tag

- In `HTML`, an `<input type="file">` lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the `File API`.
`<input type="file" />`


# Lifting State Up

- In this section, we will create a temperature calculator that calculates whether the water would boil at a given temperature.

- We will start with a component called `BoilingVerdict`. It accepts the `celsius` temperature as a prop, and prints whether it is enough to boil the water:

``function BoilingVerdict(props) {
  if (props.celsius >= 100) {
    return <p>The water would boil.</p>;
  }
  return <p>The water would not boil.</p>;
}``

Next, we will create a component called `Calculator`. It renders an `<input>` that lets you enter the temperature, and keeps its value in `this.state.temperature`.

Additionally, it renders the `BoilingVerdict` for the current input value.

##### Adding a Second Input

- Our new requirement is that, in addition to a Celsius input, we provide a Fahrenheit input, and they are kept in sync.

##### Writing Conversion Functions

- First, we will write two functions to convert from Celsius to Fahrenheit and back:

``function toCelsius(fahrenheit) {
  return (fahrenheit - 32) * 5 / 9;
}

function toFahrenheit(celsius) {
  return (celsius * 9 / 5) + 32;
}``

- It returns an empty string on an invalid `temperature`, and it keeps the output rounded to the third decimal place:

``function tryConvert(temperature, convert) {
  const input = parseFloat(temperature);
  if (Number.isNaN(input)) {
    return '';
  }
  const output = convert(input);
  const rounded = Math.round(output * 1000) / 1000;
  return rounded.toString();
}``

# Composition vs Inheritance

- React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.

##### Containment

- Some components don’t know their `children` ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.

``function FancyBorder(props) {
  return (
    <div className={'FancyBorder FancyBorder-' + props.color}>
      {props.children}
    </div>
  );
}``

- This lets other components pass arbitrary children to them by nesting the JSX:

``function WelcomeDialog() {
  return (
    <FancyBorder color="blue">
      <h1 className="Dialog-title">
        Welcome
      </h1>
      <p className="Dialog-message">
        Thank you for visiting our spacecraft!
      </p>
    </FancyBorder>
  );
}``


# Thinking in React

- React is, in our opinion, the premier way to build big, fast Web apps with JavaScript. It has scaled very well for us at Facebook and Instagram.

##### Props vs State

- There are two types of “model” data in React: props and state. It’s important to understand the distinction between the two; skim the official React docs if you aren’t sure what the difference is. See also FAQ: What is the difference between state and props?