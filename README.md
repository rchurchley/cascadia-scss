# Cascadia

Cascadia is a [SASS](http://sass-lang.com) theme to bootstrap your way to a simple responsive website. It features a header image and a mobile-friendly navigation menu (for up to four links). Check out [the demo](https://cdn.rawgit.com/rchurchley/cascadia-scss/master/demo/index.html) to see it in action.


## Usage

Compiling Cascadia requires the [`sass`](http://sass-lang.com) and [`sass-globbing`](https://github.com/chriseppstein/sass-globbing) Ruby gems to be installed on your system.

First, make sure your webpage follows the structure illustrated in `demo/index.html`. Compile the main stylesheet with
```sh
sass -r sass-globbing main.scss
```
and add the resulting CSS to your project.


## Customization

The theme can be customized by adding SASS files to a new `local` directory outside this repository. Any styles in `../local/*` will be appended to the main Cascadia stylesheet.

The color scheme (among other things) can be customized by adding SASS files to a new `local/settings` folder outside this repository. Redefining any of the following variables in `../local/settings/*` will override the default options in `partials/_base.scss`.

Default fonts:
```sass
$body-font: system, -apple-system, "Helvetica Neue", sans-serif;
$code-font: Inconsolata, monospace;
```

Default font size:
```sass
$body-font-size: large;
```

"Greyscale" colour palette, used respectively for text, minor text, borders, body background, and content background:
```sass
$base-colors: #323a44, #4f5a66, #b3bdc4, #ebf0f4, #f5f9fb;
```

"Splash" colour palette, used respectively for a, a:hover, a:visited.
```sass
$splash-colors:  #0098e9, #ff297f, #a342b4
```

The color of the header, headlines, and code.
```sass
$header-text:     nth($base-colors, 5);
$headline-color:  nth($base-colors, 2);
$code-text:       nth($base-colors, 5);
$code-background: nth($base-colors, 1);
```

Maximum width of `main`
```sass
$max-width:  640px;
```

Breakpoint below which the mobile menu is used
```sass
$breakpoint: 640px;
```

The default margin after paragraphs and other elements
```sass
$parskip: 1.25rem;
```

The proportion of `main` to be used for each gutter
```sass
$gutter-fraction: 1/16;
```
