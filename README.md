react-intro
===========

Introduction to react


Schedule
--------
* Slides up to "Why another Web Framework?"
* Find the use of react on Facebook
 * Open facebook.de and Dev Tools (maybe need to allow console for facebook)
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
* Live-Demo #1: Getting started
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
* More
  * http://facebook.github.io/react/blog/2014/03/14/community-roundup-18.html
  * Chrome plugin: http://facebook.github.io/react/blog/2014/01/02/react-chrome-developer-tools.html

