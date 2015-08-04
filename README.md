# SCSS navbar

## Templates

Start by copying our custom Wagon navbar template :

- [Wagon HTML version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar_wagon.html)
- [Wagon ERB version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar_wagon.html.erb) (an example with [devise](https://github.com/plataformatec/devise) path helpers)

Or our Bootstrap navbar template:

- [Bootstrap HTML version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar_bootstrap.html)
- [Bootstrap ERB version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar_bootstrap.html.erb) (an example with [devise](https://github.com/plataformatec/devise) path helpers)

Of course, you have to replace the assets (logo, profile picture) by your own.

## SCSS Wagon navbar

Our `_navbar_wagon.css.scss` implements style rules on the `.wagon-navbar` class.

## SCSS Bootstrap navbar

Our `_navbar_bootstrap.css.scss` implements style rules on the `.wagon-bootstrap-navbar` class. Herebelow we detail the role of each sass variable.

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


## Contribute, share your masterpiece!

Feel free to contribute to this project with pull requests, and to share with us your navbar masterpieces!

- Twitter: https://twitter.com/lewagonparis
- Facebook: https://facebook.com/lewagonformation
- Website: http://lewagon.org

Peace
