React Intro
============

## Intro
React is "A JavaScript library for building user interfaces".
React makes it very easy to create interactive UIs, and React will update and render just the right components when data changes. React has a way to manage the "state"(current status of each view) in our applications. 

## React Behind the Scenes
### React.createElement
Creating an element in React with JSX looks like this:
```jsx
const element = <h2 className="name">Name</h2>
```

The code is run through a tool that can turn JSX into JavaScript. The tool makes a JavaScript expression that creates a React element using React.createElement. The same thing in JavaScript would look like this:
```jsx
const element = React.createElement("h2", {
  className: "name"
}, "Name")
```

JSX uses className instead of class to define CSS classes.

Always start component names with a capital letter.

### ReactDOM.render
An element can be "rendered" into any DOM node using the react-dom library.
Most applications call ReactDOM.render(element, container) a single time to render the application.

## JSX Rules
1. All tags must be closed. There are two ways to close a tag.
  * Use two tags (an open tag and a close tag).
  * Use one self-closing tag
  Ex:
  ```jsx
  <div> Two Tags - Open
    <img> This would cause an error because its not closed.
    <Album /> Self-closing Tag
  </div> Two Tags - Close
  ```

2. A child tag must close before its parent. We are creating a tree structure. So the last one to open is the next one to close.

3. All JSX expressions must result in one root level element. A function can only return one value. A component is defined using a JavaScript function so the same rules apply.

4. No HTML comments.
```jsx
return (
  <div>
    <!--- Not allowed --->
    {/* Allowed */}
  </div>
)
```