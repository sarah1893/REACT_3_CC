# Add Properties to PropTypes

In the code editor, look at the property on ``MessageDisplayer``‘s ``propTypes`` object:

```
message: React.PropTypes.string 
```

What are the properties on ``propTypes`` supposed to *be*, exactly?

The *name* of each property in ``propTypes`` should be the name of an expected ``prop``. In our case, ``MessageDisplayer`` expects a ``prop`` named ``message``, so our property’s name is ``message``.

The *value* of each property in ``propTypes`` should fit this pattern:

```
React.PropTypes.expected-data-type-goes-here
```

Since ``message`` is presumably going to be a string, we chose ``React.PropTypes.string``. You can see this on line 12. Notice the difference in capitalization between the ``propTypes`` object and ``React.PropTypes``!

Each property on the ``propTypes`` object is called a ``propType``.

Select the next file in code editor, **Runner.js**. Find ``Runner``‘s ``propTypes`` object.

``Runner`` has six ``propTypes``! Look at each one. Note that ``bool`` and ``func`` are abbreviated, but all other datatypes are spelled normally.

If you add ``.isRequired`` to a ``propType``, then you will get a console warning if that ``prop`` isn’t sent.

Try to find all six ``prop``s from the ``propTypes`` object in ``Runner``‘s render function: ``this.props.message``, ``this.props.style``, etc.