# SCSS Bootstrap navbar

## Templates

Start by copying our navbar template:

- [HTML version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html)
- [ERB version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html.erb) (an example with [devise](https://github.com/plataformatec/devise) path helpers)

Of course, you have to replace the assets (logo, profile picture) by your own.

### Respect the navbar markup

For our navbar styles to apply, you have to:

- add **`class="navbar-wagon"`** to the initial Bootstrap `<nav>`
- your logo should be a `<img>` **inside** the `.navbar-brand` link.
- your profile picture should hold the class **`class="img-avatar"`**
- To apply a "button-style" to a link, add it a **`class="btn"`**


## SCSS template

Our `_navbar.css.scss` implements style rules on the `.wagon-navbar` class. Herebelow we detail the role of each sass variable.

### Navbar-Wagon SCSS variables

#### General appearance

Change your navbar background and link color, and link hover color

```scss
/* -------------------------------------
 * Colors & Fonts
 * ------------------------------------- */
$navbar-color: white;
$navbar-hover-color: #D4312D;
$navbar-font-family: "Montserrat", sans-serif; // Google fonts
$navbar-bg: transparent;
```

Change the height, spacing and borders

```scss
/* -------------------------------------
 * Box model
 * ------------------------------------- */
$navbar-height: 50px;
$navbar-vertical-padding: 5px;
$navbar-horizontal-padding: 20px;
$navbar-border-bottom-width: 0;
$navbar-border-bottom-color: grey;
```

#### Navbar button style

We give you some variables for pimping your navbar buttons.

```scss
/* -------------------------------------
 * Navbar button
 * ------------------------------------- */
$navbar-btn-height: 40px;
$navbar-btn-bg: lightgrey;
$navbar-btn-color: white;
$navbar-btn-horizontal-padding: 10px;
$navbar-btn-radius: 2px;
```

#### Profile picture

You can also change the style of your navbar profile picture playing on its radius and border

```scss
/* -------------------------------------
 * Navbar profile picture
 * ------------------------------------- */
$navbar-profile-radius: 50%;
$navbar-profile-border-color: white;
$navbar-profile-border-width: 2px;
```


## Integration in Rails

### Rails assets

In Rails, the integration is easy if you have installed `sass-rails` and `bootstrap-sass` gems. You can just add the `_navbar.scss` file to your Rails **layout stylesheets**, and then import this file in `application.css.scss`


```scss
//stylesheets/layout/_navbar.css.scss

// Our navbar SCSS code
```

```scss
//stylesheets/layout/_index.css.scss
@import "navbar";
@import "footer";
@import "sidebar";
```

```scss
//stylesheets/application.css.scss

/* -------------------------------------
 * Layout stylesheets
 * ------------------------------------- */
 @import "layout/index";

```

Here you go!

### ERB template

Don't forget to modify our [ERB template](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html.erb) carefully if you use different path helpers.

## Contribute, share your masterpiece!

Feel free to contribute to this project with pull requests, and to share with us your navbar masterpieces!

- Twitter: https://twitter.com/lewagonparis
- Facebook: https://facebook.com/lewagonformation
- Website: http://lewagon.org

Peace
