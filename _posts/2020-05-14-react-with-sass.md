---
layout: post
title:  "Set up React with SASS"
date:   2020-05-14 17:08:00
categories: programming, wxdecoder
---

# Mission

Set up a simple React website using SASS/SCSS and Bootstrap.

# Assumptions

You have...

 - An existing React web application
 - npm installed

# 1. Install node-sass

`npm install --save node-sass`

The node-sass module adds the SASS preprocessor to your React project,
allowing you to write SASS/SCSS (which browsers don't understand) and
have it converted to CSS (which they do).

# 2. Add styles to components

It's recommended to keep React components completely self-contained, styles
and all, meaning each component gets its own stylesheet. Your own setup
is completely flexible but for reference, here's how I've set up my `NavBar` component.

```
- src
  |- components
     |- NavBar
        |- NavBar.js
        |- NavBar.scss     
```

You can add component styling to `NavBar.scss` like this:

```
.navBar {
  background-color: #15354e;
}
```

And then import and use it in `NavBar.js` like this:

```
import './NavBar.scss';
...
<div className="navBar">It appears I'm a nav bar.</div>
```

# 3. Global styles

So we just said component styles should be specific to the
component, but what about global settings like colour palettes?

Although a good approach is using themes supported by libraries like Bootstrap,
for the sake of this exercise we'll assume you just want a quick way to
set a few global values and import them. We can achieve this
using SASS partials.

Create a partial file (NB. the underscore in `_colours.scss` is required):

```
- src
  |- styles
     |- _colours.scss
```

Add some code to the partial SCSS file.

```
$dark-blue: #15354e;
```

Now we import the partial into your component's stylesheet which gives
us access to the values we defined in it. In this example we're replacing
the value of `background-colour` with the imported variable.

```
@import '../../styles/_colours.scss';

.navBar {
  background-color: $dark-blue;
}
```

*NB. the official SASS docs recommend using `@use` instead of `@import`,
but at the time of writing `@use` isn't supported in node-sass.*

# And that's it!

Et voila, you've got individual component styling as well as an easy
way to deal with site-wide variables. For additional reading, check out
["Adding a SASS Stylesheet"][cra-sass]
on the create-react-app website.

[react-install]: https://reactjs.org/docs/create-a-new-react-app.html
[cra-sass]: https://create-react-app.dev/docs/adding-a-sass-stylesheet/
