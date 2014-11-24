# SASS Bootstrap navbar

## HTML template

Start by copying our navbar template:

- [HTML version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html)
- [ERB version](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html.erb)

Of course, you have to find your own logo image and replace the profile picture url by your profile picture.

### Respect our classes

For our design to work you must have the following HTML elements:

- your `nav` should have an additional **`class="navbar-wagon"`**
- your logo should be an image and have a **`id="logo"`**
- your profile picture should have a **`id="profile-pic"`**
- you button should have a **`id="nav-btn"`**


## SCSS template

Our `navbar.css.scss` implements style rules on the `.wagon-navbar` class. Herebelow we detail the purpose of each sass variable in `navbar.css.scss`.

### Wagon-navbar Sass variable

#### Navbar general appearance

Change your navbar background and text color

```scss
$color: black;
$bg: white;
```

Change the height of its content and its horizontal and vertical paddings.

```scss
$height: 40px;
$vertical-padding: 10px;
$horizontal-padding: 20px;
```

Customize your navbar bottom border if you want to:

```scss
$border-bottom-width: 0;
$border-bottom-color: transparent;
```

#### Navbar button style

Our `navbar.scss` gives you lot of flexibility for pimping your navbar button.

```scss
$btn-height: 40px;
$btn-bg: lightgrey;
$btn-color: black;
$btn-horizontal-padding: 10px;
$btn-top-border-width: 0;
$btn-top-border-color: transparent;
$btn-right-border-width: 0;
$btn-right-border-color: transparent;
$btn-bottom-border-width: 3px;
$btn-bottom-border-color: grey;
$btn-left-border-width: 0;
$btn-left-border-color: transparent;
```

#### Profile picture style

You can also pimp your navbar profile picture by changing its radius and its border

```scss
// Set your profile picture
$profile-radius: 20%;
$profile-border-color: white;
$profile-border-width: 2px;
```


## Integration in Rails

### Rails assets

In Rails, the integration is easy if you have installed `sass-rails` and `bootstrap-sass` gems. You can just add the `navbar.scss` file to your Rails stylesheets, and then import this file in `application.css.scss`


```scss
//application.css.scss

// "bootstrap-sass" imports
@import "bootstrap-sprockets";
@import "bootstrap";

// Import our navbar.scss after bootstrap
@import "navbar";
```

Here you go!

### ERB template

Don't forget to modify our [ERB template](https://github.com/lewagon/awesome-navbars/blob/master/templates/_navbar.html.erb) carefully using Rails helpers.

## Contribute, share your masterpiece!

Feel free to contribute to this project with pull requests, and to share with us your navbar masterpieces.

- Twitter: https://twitter.com/lewagonparis
- Facebook: https://facebook.com/lewagonformation
- Website: http://lewagon.org

Peace!
