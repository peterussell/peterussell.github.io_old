---
layout: post
title:  "Set up React with SASS"
date:   2020-05-14 17:08:00
categories: programming, wxdecoder
---

# Mission

Set up a simple React website using SASS/SCSS and Bootstrap.

# Assumptions

An existing React web application (see the docs on
[How to create a react app][react-install]  if you need help), and 
`npm` installed.

# 1. Install node-sass

`npm install --save node-sass`

The node-sass module adds the SASS preprocessor to your React project,
allowing you to write SASS/SCSS (which browsers don't understand) and
have it come out as CSS (which browser do understand).

# 2. Add styles to components

It's generally recommended to keep React components completely
self-contained, which implies that each component should have its
own stylesheet. For example, this is how I've implemented my `NavBar`
component.

```
- src
  |- components
     |- NavBar
        |- NavBar.js
        |- NavBar.scss     
```

SCSS can be added to `NavBar.js`...

```
.navBar {
  background-color: #15354e;
}
```

... and then imported and used in `NavBar.js`

```
import './NavBar.scss';
...
<div className="navBar">It appears I'm a nav bar.</div>
```

# 3. Adding global styles

So what about global styling like colour palettes, stored in variables
inside SASS partials?

Create a partial file (NB. the underscore tells the preprocessor that
the file is meant to be included in another file, and don't create a
standalone CSS file for it)...

```
- src
  |- styles
     |- _colours.scss
```

... add some code ...

```
$dark-blue: #15354e;
```

... then load the partial into your component's stylesheet, and use
the variable. In this example, we're replacing the `background-colour`
with the imported variable.

```
@import '../../styles/_colours.scss';
...
.navBar {
  background-color: $dark-blue;
}
```

# And that's it!

Et voila, you've got individual component styling as well as an easy
way to deal with site-wide variables. For additional reading, check out [Adding a SASS Stylesheet][cra-sass]
on the create-react-app website.

[react-install]: https://reactjs.org/docs/create-a-new-react-app.html
[cra-sass]: https://create-react-app.dev/docs/adding-a-sass-stylesheet/
