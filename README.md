# MaterialZ
<img src="https://raw.githubusercontent.com/ZMYaro/materialz/master/logo/banner.svg" width="680" alt="MaterialZ logo." />

MaterialZ is a CSS library that implements [Google's Material Design guidelines](https://material.io/design/introduction) in plain CSS.


## Material-ize your site
If you want Material-/Paper-themed HTML elements on your page, you just need to include “**material-elements.css**”, which styles most basic HTML elements.  Add that style sheet to an unstyled page, and it should “just work”!

[See all elements and example code at materialz.dev/#elements →](https://materialz.dev/#elements)

## Add Material widgets
You can use widgets such as action bars, lists, and cards by including “**material-widgets.css**” and specifying classes:
* To add a top app bar, add an element with the `appBar` class (e.g., `<header class="appBar">`).
* To add a toolbar, add an element with `role="toolbar"` (e.g., `<div role="toolbar">`).  Toolbar buttons are flat and round by default.
  - An Android action bar is frequently just an app bar with toolbar buttons - `<header class="appBar" role="toolbar">`.
* To add a list, add a `<ul>` or `<ol>` element with the `list` class (e.g., `<ul class="list">`).
* To add a card, add the `card` class to an element.  You can make it fill the width of narrow windows by adding the `full-width` class as well.  You may also wish to use the depth classes to “raise” the card as well (see below).
* To add a circular progress spinner, add a `<progress>` element with the `circular` class (e.g., `<progress class="circular">`).
* To add a toggle switch, add a checkbox with the `switch` class (e.g., `<input type="checkbox" class="switch" />`).

Note: adding the widgets stylesheet will automatically add padding to the `body` for the default app bar size.

[See all widgets and example code at materialz.dev/#widgets →](https://materialz.dev/#widgets)

## Add depth
You can add shadows to elements by including “**material-depth.css**” and then applying the classes `z1`-`z5`.  These are best used with `<button>`s (e.g., `<button class="z1">` for a raised button), `.card`s (e.g., `<div class="card z2">`), and `.appBar`s (e.g., `<header class="appBar z3">`).

[See demo and example code at materialz.dev/#depth →](https://materialz.dev/#depth)

## Add dark theme
You can enable an instant dark theme by including “**material-dark.css**”.  Import it with the `prefers-color-scheme: dark` media query to automatically respect the user's system dark theme setting (on OSes/browsers that support it).

[See demo and example code at materialz.dev/#darktheme →](https://materialz.dev/#darktheme)

## Make it work a little better in older mobile browsers
One great use of MaterialZ is to make mobile web apps look like native Android 5+ apps.  MaterialZ includes a script to make sure all widgets respond to touch properly in mobile WebKit (Mobile Safari, AOSP Browser, earlier Chrome for Android) by overriding the default tap delay.
* Make sure you include the “**material-touch.js**” file.
* Add a script tag to your page: `<script type="text/javascript" src="material-touch.js"></script>`.

## Make it work a little better in older desktop browsers
You can add the “**fix-\*.css**” stylesheets to fix certain issues ith older browsers, such as IE < 9 and Safari < 6, if you need to support those, however you should only load those stylesheets in those browsers, as they include overrides for better styles used in newer browsers.

## The Roboto Font
“**material-elements.css**” imports basic Roboto and Roboto Mono by default.  If you need more weights or character sets, you can load them through [Google Web Fonts](https://fonts.google.com/specimen/Roboto).

## Known issues
* Certain form elements (checkboxes, radio buttons) are only properly themed in WebKit-derived browsers (e.g. Safari, Chrome, new Edge, newer Opera) and newer versions of Firefox, and partially themed in Presto (older Opera) and the latest versions of Trident/EdgeHTML (IE10+, Edge Legacy).
* Certain form elements, such as range sliders, are unsupported in some older browsers.
* Accent color custom property only partially works in some older versions of WebKit (Safari).

The above issues are the result of browser limitations or lack of documented solutions.

## Contributing to MaterialZ
Contributions to this project are welcome.  Please follow standard [commit guidelines](http://git-scm.com/book/ch5-2.html#Commit-Guidelines).
