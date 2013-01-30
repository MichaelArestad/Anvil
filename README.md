![Hammer icon](http://anvil.michaelarestad.com/img/anvil.svg "Clang!")

# A front-end template for Hammer.

## Anvil includes

1. [HTML5 Boilerplate](http://html5boilerplate.com)
   * jQuery
   * Modernizr
   * normalize.css
   * print styles
   * Google Analytics
   * a whole bunch of other cool stuff

2. SASS (SCSS)
   * optional mixin library I wrote
   * optional partial style sets
     * buttons
     * forms
     * responsive Bootstrap Grid generator
     * hamburger mmmmmmmenu

3. Comments everywhere
   * All single-line comments `//` in the SCSS files are stripped in the build files.

4. `display.html`
   * includes just about every non-depreciated HTML element on one page for quick styling.

## Anvil install and publish instructions

1. Download the latest version of [Hammer](http://hammerformac.com/) from the App Store.
2. Download the latest version of Anvil and rename the root folder to the name of your site.
3. Add the site to Hammer.
4. Build your awesome website.
5. Publish the contents of the `Build` folder.

## HTML goodies

### index.html

If you take a look at `index.html` in your editor, you'll find it is mostly Hammer methods and helpers. See [Hammer's Help Docs](http://help.hammerformac.com/) for full documentation.

The most basic and super useful helpers are the HTML includes `_head`, `_nav`, and `_footer`.

I've added a couple handy variables as well. 

* `$title` sets the page title. If you don't set the title, it falls back to "Anvil." Change the default value in `_head.html`.
* `$body-class` sets the body class(s) to whatever you like. It defaults to "default." Change the default value in `_head.html`.

Take a look in `_head.html` and `_footer.html` to see how stylesheets and javascript files are pulled using the Hammer syntax.

### display.html

Personally, I prefer to do a good portion of my styling before I add any classes. To make this easier on myself, I've added just about every non-depreciated HTML element to this single page. Ideally, you would use this to set your global styles in `_base.scss`.

You can search for any element by tag, `<pre>` and most elements by namde, `unordered list`.

Under the heading **Custom class elements**, you will find any HTML elements that I've added custom classes to. These show off some partials and any javascript I've added that rely on classes.

### hamburger.html

This shows off a responsive menu very similar to a bagillion app hamburger menus. Hamburger refers to the three bar menu icon. It is almost entirely based on Tim Pietrusky's [Off Canvas menu](http://codepen.io/TimPietrusky/pen/CLIsl). Customize it in `_menu-hamburger.scss`.

### 404.html

Straight from HTML5 Boilerplate. Except for really minor changes. I suggest making it into something surprising and useful to visitors with your webby skills.

## Styling Anvil

You'll notice style.css and `style.scss` in the CSS folder. Hammer requires a `style.css` file to compile SCSS files to. It gets overwritten, so it doesn't matter what is in `style.css` as long as the file is there.

`style.css` is where every SCSS file is pulled into and determines the order the styles appear on the build `style.css` file. The comments provide brief descriptions of what each imported file contains. Note that all single-line comments are stripped from the build file.

Put all your main styles in `_main.scss`. If you're unfamiliar with SASS, don't sweat it. Standard CSS works just fine.

For those of you who love your SASS, check out `_variables.scss` and `_mixins.scss` to see some of my shortcuts. You can also just remove `_mixins.scss` and use Hammer's built-in [Bourbon](http://bourbon.io/) mixins.

### SCSS Partials

These are optional sections that might come in handy and save you a little styling time. I'll probably add more or remove them depending on the responses I get.

#### Included Partials
`_buttons.scss`  
Two button sets are included. Form buttons with out classes and a button class for styling a links or whatever you like as a button.

`_form.scss`  
Two form element sets are included. The default active one is for all form elements without the need for classes. The commented out section below is useful when you want to make multiple form styles.

`_grid-responsive.scss`  
Super sexy Bootstrap-style grid generator. It uses the same syntax as the responsive Bootstrap grids. You can change the variable values to generate your own preferred grids. This currently does not support fluid, percentage-based, grids. Yet.

`_menu-hamburger.scss`  
This utilizes a checkbox hack in order to create a Google or Facebook hamburger-style menu. See it in action on `hamburger.html`. Note that using it as a responsive menu isn't exactly the most semantic option, however, it sure is neato.

## Things to note
If you opt to use [Bourbon](http://bourbon.io/) mixins and remove my mixins, you will need to go through and change almost all of the mixins throughout the stylesheets.

If you don't plan on using one or more of the partials or SCSS files, simply comment them out. Again, anything commented out with a single-line comment `//` will not end up in the final build.

Go to HTML5 Boilerplate's website, if you haven't already, and familiarize yourself with the endless goodies they've put together. Most of those are in Anvil.

I made this entirely for myself. I <del>encourage</del> **dare** you to make something even better.