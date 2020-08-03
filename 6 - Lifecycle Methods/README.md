# What's a Lifecycle Method?

*Lifecycle methods* are methods that get called at certain moments in a component’s life.

You can write a lifecycle method that gets called right before a component renders for the first time.

You can write a lifecycle method that gets called right *after* a component renders, every time *except* for the first time.

You can attach lifecycle methods to a lot of different moments in a component’s life. This has powerful implications!

# Mounting Lifecycle Methods

There are three categories of lifecycle methods: *mounting, updating*, and *unmounting*. This lesson is about the first category: *mounting* lifecycle methods.

A component “mounts” when it renders for the first time. This is when *mounting lifecycle methods* get called.

There are three mounting lifecycle methods:

    - componentWillMount
    - render
    - componentDidMount
When a component *mounts*, it automatically calls these three methods, in order.

# componentWillMount

The first *mounting* lifecycle method is called ``componentWillMount``.

When a component renders for the first time, ``componentWillMount`` gets called right *before* render.

Look at **Example.js**, and follow these steps:

1. On lines 14-17, ``<Example />`` is rendered for the first time. ``<Example />``‘s *mounting* period begins.
   
2. ``<Example />`` calls the first mounting lifecycle method, ``componentWillMount``.
   
3. ``componentWillMount`` executes, and an alert appears on the screen. (lines 5-7)

4. After ``componentWillMount`` has finished, ``<Example />`` calls the second mounting lifecycle method: render.

5. `<h1>Hello world</h1>` appears on the screen (lines 9-11)
   
6. Two seconds later, ``<Example />`` renders again (lines 20-22). ``componentWillMount`` does NOT get called, because mounting lifecycle events only execute the first time that a component renders.

You can call ``this.setState`` from within ``componentWillMount``!

Look at **Example2.js** for an example of ``this.setState`` inside of ``componentWillMount``. See if you can follow how ``<Example2 />`` would render ``<h1>Hello world</h1>``.


# componentDidMount

The final mounting lifecycle method is called ``componentDidMount``.

When a component renders for the first time, ``componentDidMount`` gets called right after the HTML from ``render`` has finished loading. Look in the code editor for an example of ``componentDidMount``.

``componentDidMount`` gets used a lot!

If your React app uses AJAX to fetch initial data from an API, then ``componentDidMount`` is the place to make that AJAX call. More generally, ``componentDidMount`` is a good place to connect a React app to external applications, such as web APIs or JavaScript frameworks. ``componentDidMount`` is also the place to set timers using ``setTimeout`` or ``setInterval``.

If that sounds vague, don’t worry. You’ll put lifecycle methods into practice in this course’s final project! Not to mention in the real world…