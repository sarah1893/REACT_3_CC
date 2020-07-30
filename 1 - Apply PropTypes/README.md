# Apply PropTypes

In the code editor, take a look at ``MessageDisplayer‘s`` render function.

Notice the expression ``this.props.message``. From this expression, you can deduce that ``MessageDisplayer`` expects to get passed a ``prop`` named ``message``. Somewhere, at some time, this code is expected to execute:

```
<MessageDisplayer message="something" />
```

If a component class expects a ``prop``, then you can give that component class a ``propType``!

The first step to making a ``propType`` is to search for a property named ``propTypes`` on the instructions object. If there isn’t one, make one! You will have to declare it after the close of your component declaration, since it will be a static property.

See the example of a ``propTypes`` property on lines 11-13. Notice that the value of ``propTypes`` is an object, not a function!

The second step is to add a property to the ``propType`` object. For each ``prop`` that your component class expects to receive, there can be one property on your ``propTypes`` object.

``MessageDisplayer`` only expects one ``prop``: `message`. Therefore, its ``propTypes`` object only has one property.