#MaterialZ

MaterialZ is a CSS library that implements [Google's Material Design guidelines](http://google.com/design) in plain CSS.


##Material-ize your site
If you want Material-/Paper-themed HTML elements on your page, you just need to include “material-elements.css”, which styles most basic HTML elements.

##Add Material widgets
You can use widgets such as action bars, lists, and cards by adding “material-widgets.css” and specifying classes:
* To add a top app bar, add a `<header>` element with the class `appBar` (e.g., `<header class="appBar">`).
  - (Use a `<footer>` element for a bottom action bar like in Android 4.)
* To add a list, add a `<ul>` or `<ol>` element with the class `list` (e.g., `<ul class="list">`).
* To add a card, add the `card` class to an element.  You may wish to use the depth classes to "raise" the card as well (see below).

Note: adding the widgets stylesheet will automatically add padding to the `body` for the default app bar size.

##Add depth
You can add shadows to elements with classes `z1`-`z5`.  These are best used with `<button>`s and `.card`s (e.g., `<button class="z1">` for a raised button, `<div class="card z2">`).

##Make it work on older mobile browsers
One great use of MaterialZ is to make mobile web sites look like native Android L apps.  MaterialZ includes a script to make sure all widgets respond to touch properly in mobile WebKit (Mobile Safari, Android Browser, Chrome for Android).
* Make sure you include the material-touch.js” file in your project.
* Add a script tag to your page: `<script type="text/javascript" src="material-touch.js"></script>`.

##The Roboto Font
material-elements.css imports basic Roboto by default.  If you need more weights or character sets, you can load them through [Google Web Fonts](http://google.com/fonts#UsePlace:use/Collection:Roboto).

##Known issues
* Certain elements, including checkboxes and range sliders are not completely themed (yet).
* Certain form elements (checkboxes, radio buttons) are only properly themed in WebKit-based browsers (e.g. Safari, Chrome) and partially themed in Presto (older Opera) and the latest version of Trident (IE10+).
* Certain form elements, such as range sliders, are unsupported in some older browsers.

The above issues are the result of browser limitations or lack of documented solutions.

##Contributing to MaterialZ
Contributions to this project are welcome.  Please follow standard [commit guidelines](http://git-scm.com/book/ch5-2.html#Commit-Guidelines).
