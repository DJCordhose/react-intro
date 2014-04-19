react-intro
===========

Introduction to react


Preparation
-----------
* While having internet connection for sure
  * Open http://facebook.github.io/react/


Schedule
--------
* Slides up to "Another Web Framework?"
* Find the use of react on Facebook
 * Open facebook.de and Dev Tools (maybe need to allow console for facebook)
 * How many reactive elements? document.querySelectorAll('[data-reactid]').length
 * Array.prototype.slice.call(document.querySelectorAll('[data-reactid]')).forEach(function (node) {node.style.color = 'red'});
 * setInterval(function() {Array.prototype.slice.call(document.querySelectorAll('[data-reactid]')).forEach(function (node) {node.style.color = 'red'})}, 1000);
* Concepts in slides
* Live-Demo #0: Start Page
  * http://facebook.github.io/react/
  * React.createClass
    * creates a new component based on the given spec
    * must implement render: creates a virtual DOM tree (maybe using JSX)
    * INPUT: input data can be accessed using this.props
    * STATE: component data read using this.state and set using this.setState
      * when state changes render will be called again and diff for virtual DOM is calculated and applied
      * use seconds elapsed example to show which parts of the DOM are updated
        * inspect element and add color style to span around changed seconds and show it remains unchanged
  * Show full app
    * Reference to other component: <TodoList items={this.state.items} />
      * Uses TodoList class and adds items to props
* Optionally Live-Demo #1: Getting started
  * JSX
  * http://facebook.github.io/react/docs/top-level-api.html
  * React.renderComponent(ReactComponent component, DOMElement container)
  * React.renderComponentToString: for server side rendering
* Live-Demo #2: React-TodoMVC
  * js/utils.js: helpers
  * js/todoModel.js
    * model in plain JS
    * react works with all kinds of model technologies
    * uses 'extend' from utils extensively to work with immutable data structures
  * js/app.jsx
    * componentDidMount: routing
    * render: creating the app
    * Listening to model change: model.subscribe(render);
    * setState might batch updates, so add a callback when you want to execute code when setState has done its work
  * js/footer.jsx: nothing new here
  * js/todoItem.jsx
    * shouldComponentUpdate: performance optimization that checks if anything has changed at all
* Live-Demo #3: Server Side rendering
  * start react-server-example in code (from https://www.npmjs.org/package/react-server-example)
    * Change: deferred client side rendering (instead print out part for rendering on console)
  * Load application in browser (localhost:3000)
  * in Developer tools: Show there is no click handler attached
  * Change color of an item
  * start client side rendering (by executing printed rendering part)
  * Show color stays the same
  * in Developer tools: Show there is now is a click handler for the whole component
  * Click and add items
  * Show color still stays the same
* More
    * React.addons.classSet: Utility function to set css classes
  * http://facebook.github.io/react/blog/2014/03/14/community-roundup-18.html
  * Chrome plugin: http://facebook.github.io/react/blog/2014/01/02/react-chrome-developer-tools.html
   * http://augustl.com/blog/2014/jdk8_react_rendering_on_server/?utm_source=javascriptweekly&utm_medium=email
      * Jdk 8, Nashorn, Closure, React.js
   * https://news.ycombinator.com/item?id=7489959
   * https://speakerdeck.com/shieldo/react-glasgow-js-1st-april-2014
   * https://github.com/reactjs/express-react-views
   * http://eflorenzano.com/blog/2014/04/10/react-part-2-build-system/
