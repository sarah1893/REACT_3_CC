# PropTypes in Stateless Functional Components

Remember *stateless functional components*? You can see some familiar ones in **Example.js**.

How could you write ``propTypes`` for a stateless functional component?

```
// Usual way:
class Example extends React.component{
}
Example.propTypes = {

};


// Stateless functional component way:
const Example = (props) => {
  // ummm ??????
```

It turns out the process is fairly similar. To write ``propTypes`` for a stateless functional component, you define a ``propTypes`` object as a property of the *stateless functional component itself*. Here’s what that looks like:

```
const Example = (props) => {
  return <h1>{props.message}</h1>;
}

Example.propTypes = {
  message: React.PropTypes.string.isRequired
};
```