<pre>
 █    ██ ▄▄▄█████▓ ██▓ ██▓     ██▓▄▄▄█████▓ ▄▄▄       ██▀███   ██▓ ▄▄▄       ███▄    █ 
 ██  ▓██▒▓  ██▒ ▓▒▓██▒▓██▒    ▓██▒▓  ██▒ ▓▒▒████▄    ▓██ ▒ ██▒▓██▒▒████▄     ██ ▀█   █ 
▓██  ▒██░▒ ▓██░ ▒░▒██▒▒██░    ▒██▒▒ ▓██░ ▒░▒██  ▀█▄  ▓██ ░▄█ ▒▒██▒▒██  ▀█▄  ▓██  ▀█ ██▒
▓▓█  ░██░░ ▓██▓ ░ ░██░▒██░    ░██░░ ▓██▓ ░ ░██▄▄▄▄██ ▒██▀▀█▄  ░██░░██▄▄▄▄██ ▓██▒  ▐▌██▒
▒▒█████▓   ▒██▒ ░ ░██░░██████▒░██░  ▒██▒ ░  ▓█   ▓██▒░██▓ ▒██▒░██░ ▓█   ▓██▒▒██░   ▓██░
░▒▓▒ ▒ ▒   ▒ ░░   ░▓  ░ ▒░▓  ░░▓    ▒ ░░    ▒▒   ▓▒█░░ ▒▓ ░▒▓░░▓   ▒▒   ▓▒█░░ ▒░   ▒ ▒ 
░░▒░ ░ ░     ░     ▒ ░░ ░ ▒  ░ ▒ ░    ░      ▒   ▒▒ ░  ░▒ ░ ▒░ ▒ ░  ▒   ▒▒ ░░ ░░   ░ ▒░
 ░░░ ░ ░   ░       ▒ ░  ░ ░    ▒ ░  ░        ░   ▒     ░░   ░  ▒ ░  ░   ▒      ░   ░ ░ 
   ░               ░      ░  ░ ░                 ░  ░   ░      ░        ░  ░         ░ 
                                                                                       
  █████▒██▀███   ▄▄▄       ███▄ ▄███▓▓█████  █     █░ ▒█████   ██▀███   ██ ▄█▀         
▓██   ▒▓██ ▒ ██▒▒████▄    ▓██▒▀█▀ ██▒▓█   ▀ ▓█░ █ ░█░▒██▒  ██▒▓██ ▒ ██▒ ██▄█▒          
▒████ ░▓██ ░▄█ ▒▒██  ▀█▄  ▓██    ▓██░▒███   ▒█░ █ ░█ ▒██░  ██▒▓██ ░▄█ ▒▓███▄░          
░▓█▒  ░▒██▀▀█▄  ░██▄▄▄▄██ ▒██    ▒██ ▒▓█  ▄ ░█░ █ ░█ ▒██   ██░▒██▀▀█▄  ▓██ █▄          
░▒█░   ░██▓ ▒██▒ ▓█   ▓██▒▒██▒   ░██▒░▒████▒░░██▒██▓ ░ ████▓▒░░██▓ ▒██▒▒██▒ █▄         
 ▒ ░   ░ ▒▓ ░▒▓░ ▒▒   ▓▒█░░ ▒░   ░  ░░░ ▒░ ░░ ▓░▒ ▒  ░ ▒░▒░▒░ ░ ▒▓ ░▒▓░▒ ▒▒ ▓▒         
 ░       ░▒ ░ ▒░  ▒   ▒▒ ░░  ░      ░ ░ ░  ░  ▒ ░ ░    ░ ▒ ▒░   ░▒ ░ ▒░░ ░▒ ▒░         
 ░ ░     ░░   ░   ░   ▒   ░      ░      ░     ░   ░  ░ ░ ░ ▒    ░░   ░ ░ ░░ ░          
          ░           ░  ░       ░      ░  ░    ░        ░ ░     ░     ░  ░            
                                                                                       
</pre>

UCSSM is a CSS framework and a methodology for developing responsive, mobile first projects on the web.

Unlike other similar projects such as Bootstrap or BEM, UCSSM focuses on the [utilitarian philosophy of CSS](http://minid.net/2019/04/07/the-css-utilitarian-methodology/): which advocates using atomized classes with individual utility applied to the element instead of creating an initial set of predefined structures, styles and effects, thus increasing the overall size of the CSS file and the time it takes to maintain it or resume  development.

Websites and apps that were made with UCSSM have generally offered higher performance results: the painting speed will be reduced by half or more than that; the rendering time will be around 400% faster and the size of CSS files will remain smaller and easy to maintain.

## Installation

Assuming you already have a CSS folder in your project, that compiles Sass:

1. Clone this repo on your `/stylesheet/` folder.
2. Create a new file as a main `.scss`, ex. `styles.scss`.
3. Append `.scss` to the template files: `config_css`, `config_normalizer` and `config_vars`.
4. Open your main `styles.scss` and `@import` each template.

The correct order in your `styles.scss` must be:

<pre>
@import 'utilcss/config_vars.scss';
@import 'utilcss/config_css.scss';
@import 'utilcss/config_normalizer.scss';
@import 'utilcss/util.scss';

/* my style here */
</pre>

## Usage

You can read an introductory [article about the Utilitarian CSS Methodology](http://minid.net/2019/04/07/the-css-utilitarian-methodology/) to learn how to build with this new approach.

Once you have imported all the files into your main `styles.scss` you can open `config_css.scss` in order to start activating all the CSS properties you need for your project. You can start with the basic one, `display`, by searching the variable `$config-display` and change its value to `true`:

<pre>
$config-display: true;
</pre>

The next step is to open `$config_vars.scss` and search for `$displays`. Uncomment some values:

<pre>
$displays: (
  // inline,
  block,
  // contents,
  flex,
  grid,
  // inline-block,
  // inline-flex,
  // inline-grid,
  // inline-table,
  // list-item,
  // run-in,
  // table,
  // table-caption,
  // table-column-group,
  // table-header-group,
  // table-row-group,
  // table-cell,
  // none,
  // initial,
  // inherit
);
</pre>

Refresh your website and open the compiled version of `styles.css` it must compile:

<pre>
.display--block { display: block }
.display--flex { display: flex }
.display--grid { display: grid }
</pre>

Now you can add this classes to your project:

<pre>
   &lt;span class="display--block"&gt;This is a block now &lt;/span&gt;
</pre>

You can comment/uncomment any map value and Compass will compile automatically the CSS for you on the next build making easy to check which properties are you supporting for your projects.

You can add new values to any map, for the case of `$colors`, `$margins`, etc.

By doing this, your CSS output will be really strict and you will only dispose those properties that you need.


## The grid system

This framework let you use all the power of CSS-Grid. On `config_vars` you can find the `$columns:` variable with the amount of columns your grid must support. If you change this number, it means you compile as much `grid-template-columns--[NUMBER]` as this variable needs. 


## List of supported properties

* align-content
* align-items
* align-self
* background-origin
* background-size
* background-color
* background-repeat
* background-clip
* border-collapse
* border-radius
* border-style
* border-width
* box-decoration-break
* box-sizing
* color
* column-count
* column-fill
* column-gap
* column-rule-style
* column-rule-color
* display
* flex-direction
* flex-grow
* flex-wrap
* font-weight
* font-style
* grid-auto-flow
* grid-column
* grid-column-gap
* grid-gap
* grid-row
* grid-row-gap
* grid-template-columns<sup>1</sup>
* grid-template-rows<sup>2</sup>
* justify-content
* justify-items
* justify-self
* object-fit
* overflow
* overflow-x
* overflow-y
* pointer-events
* position
* text-align
* text-overflow
* text-transform
* vertical-align
* visibility
* white-space
* width
* word-wrap

The framework contains a normalizer module.

<sup>1</sup> Can be used as `sm-[property]`, `md-[property]`

<sup>2</sup> Also can be triggered by responsive steps