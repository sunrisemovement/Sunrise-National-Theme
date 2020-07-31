# Project Management

Figma Design Files
https://www.figma.com/file/IfGUJ91VgixZ9wG94PHZZk/Sunrise-National-Hub-Pages-Current?node-id=193%3A47

Notion Wiki
https://www.notion.so/evanmceldowney/Sunrise-National-Website-80a2f109ea7d42c181fbb19901efd354

Airtable Development Manager (for editability ask Evan)
https://airtable.com/shrWWYWcB2LLxr8Le

# WordPress Local Setup

Download local by flywheel, install, and run a local instance
https://localwp.com/

Import theme in your site in app/public/wp-content/themes/ using
git clone https://github.com/sunrisemovement/Sunrise-National-Redesign.git

Activate theme in the wordpress admin

Import wordpress content using wordpress importer with file from https://www.notion.so/evanmceldowney/Wordpress-Content-July-23rd-38536a2f5a46498093d623d439256f3f

## Initial Setup

This theme uses [WPGulp](https://github.com/ahmadawais/WPGulp) for "An advanced & extensively documented Gulp WordPress workflow".

To start developing your theme follow these instructions:

1. Open `wpgulp.config.js` and edit the `projectURL` variable.
1. Run `npm i` in the same directory as this theme.
1. Run `npm start`.

Once these steps are complete, you only need to run `npm start` moving forward.

## Assets

### Styles

- `assets/css/style.scss` is the main stylesheet that contains all partials. This is compiled into `style.css`.
- `assets/css/bootstrap` contains the Bootstrap core `.scss` files and should not be edited. Instead use `assets/css/base/_bootstrap_overrides.scss` to override the default variables.
- Feel free to add additional partials to this theme.

### Javascript

- `assets/js/custom` contains any custom javascript files. By default it comes with two scripts generated by [Underscores](https://underscores.me/). All files in this directory are compiled into `assets/js/custom.js` and `assets/js/custom.min.js`. By default the themes loads `assets/js/custom.min.js`.
- `assets/js/vendor` contains any vendor javascript files. This is also where `bootstrap.js` is loaded. All files in this directory are compiled into `assets/js/vendor.js` and `assets/js/vendor.min.js`. By default the themes loads `assets/js/vendor.min.js`.

### Images

- Place any images into `assets/img/raw`. From there, they will be optimized and placed in `assets/img`.

## Overriding Bootstrap Variables

If you wish to override Bootstrap's default variables, do so by redeclaring those variables in `assets/css/base/_bootstrap_overrides.scss`. Use `assets/css/bootstrap/_variables.scss` as a reference for all existing variables, but **DO NOT** update this or any other file located in `assets/css/bootstrap/`.

[More information on variable defaults](https://getbootstrap.com/docs/4.3/getting-started/theming/#variable-defaults)

For more questions
https://getbootstrap.com/docs/4.0/getting-started/introduction/

## Automatic Form Styling

Bootstrap does not style form elements be default. Instead, a developer must manually add the [correct classes](https://getbootstrap.com/docs/4.3/components/forms/#form-controls) to each form element.

In an effort to streamline this process, this theme automatically styles all form elements by extending the `.btn` class on these elements. These styles are located in `assets/css/base/_forms.scss`.

## Base WordPress Styles

Some css classes are [required by WordPress](https://codex.wordpress.org/CSS#WordPress_Generated_Classes) and therefore should be included in a WordPress theme. These, and other WordPress specific styles generated by [Underscores](https://underscores.me/) are located in `assets/css/base/_wordpress.scss`.
