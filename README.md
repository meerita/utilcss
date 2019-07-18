The Utilitarian CSS Framework (UCSSM) is a Functional CSS framework and a methodology for developing any website with incredible loading, rendering and painting performance, helping developers to work over time without having to carry architectural problems, technical debt or legacy problems. Yes, you can do responsive to.

Unlike other similar projects such as Bootstrap or BEM, UCSSM focuses on the [utilitarian/functional philosophy of CSS](http://minid.net/2019/04/07/the-css-utilitarian-methodology/): which advocates using atomized classes with individual utility applied to the element instead of creating an initial set of predefined structures, styles and effects, thus increasing the overall size of the CSS file and the time it takes to maintain it or resume  development.

Websites and apps that were made with UCSSM have generally offered incredible performance results: the painting speed will be reduced by half or more than that; the rendering time will be around 400% faster of your previous projects and the size of CSS files will remain smaller by x10 and it will be easy to maintain.

## Setup

Setting up UCSS is really straightforward if you already worked with SCSS. Assuming you already have a CSS folder in your project, that compiles Sass:

1. Clone this repo on your `/stylesheet/` folder.
2. Create a new file as a main `.scss`, ex. `styles.scss`.
3. Copy `config_css`, `config_normalizer` and `config_vars` to your `/stylesheet/` folder.
4. Append `.scss` to the template files: `config_css`, `config_normalizer` and `config_vars`.
5. Open your main `styles.scss` and `@import` each template and `util.css`.

The correct order in your `styles.scss` must be:

<pre>
@import 'config_vars.scss';
@import 'config_css.scss';
@import 'config_normalizer.scss';
@import 'utilcss/util.scss';

/* my style here */
@import 'custom.scss';
</pre>

If you don't copy the variables files outside the repo you will have problems when you commit your project, since you will have a cloned repo on your git repo. To avoid problems, it is better to have those files copied outside and be part of your repo in case you want update the framework in the future.

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

This framework let you use all the power of CSS-Grid without reinventing the wheel. This grid system is natural CSS from the CSS Grid Spec, this means the naming also respect the structure of the original CSS Grid properties. Since CSS Grid is supported in all browsers by now, it is a good replacement and also it covers legacy support, so you don't need to replace the class names once grid- prefix goes deprecated.

To start a grid in any block or inline element, you must activate the grid properties, make sure you have the first one, `display--grid` from the previous section on this README.

<pre>
&lt;div class="display--grid"&gt;
  This is a grid now
&lt;/div&gt;
</pre>

The next step is to edit `config_css` and activate the level of responsiveness for the columns or rows of your grid. Also, let's activate `gap--` property. In the config file, find `$config-gap`, `$config-grid-sm`, `$config-sm-grid-template-columns` and set it to `true`.

Now in your DIV element use the properties. Since by default we have 12 columns in our variables file, let's make the grid 6 columns by using the `template-columns--` property (you don't need to append the grid-).

<pre>
&lt;div class="display--grid sm-template-columns--6"&gt;
  Now this grid has 6 columns.
&lt;/div&gt;
</pre>

Now we have a 6 column grid that works from mobile devices. Let's add a gap 8px gap in between the columns, but first, activate the gap scales in the `config_vars` file under `$gap-scales` map:

<pre>
$gap-scales: (
  // 0,
  // 4,
  8,
  // 16
  );
</pre>

You can do your own gap values any time. Just add them to the map and they will build themselves in the next compilation. Now it's time to add the gap into our grid:

<pre>
&lt;div class="display--grid sm-template-columns--6 gap--8"&gt;
  Now this grid has 6 columns and 8px gap.
&lt;/div&gt;
</pre>

This is how grids can be made in UCSS. Plainly simple. The gap property is not responsive. Most of the projects they use the same gap pattern for everything, so if you need a particular change, I recommend you to use a c-classname to do that.

Let's say you want 2 columns in mobile and 6 in desktop. You need then to activate the `$config-grid-md`, `$config-md-grid-template-columns` (for tablets and small desktop onwards) grid config, in the `config_css` file. After you do that, now add the classes to your grid:

<pre>
&lt;div class="display--grid sm-template-columns--2 gap--8 md-template-columns--6 gap--8"&gt;
  Now this grid has 2 columns in mobile and 6 in desktops with 8px gap.
&lt;/div&gt;
</pre>

The grid system is infinitely usable. You can use all css grid- properties in different responsive steps and be sure this will never broke your website, even when you update the framework due its thoughtful legacy support.

## Responsive

There are a handful of properties that can be used responsively. We decided to not make everything responsive for the sake of keeping the generated code clean and not bloated and to make sure developers only have to take care the minimum. In our tests and analysis, the majority of the developers use way more `display`, `grid` properties than other more cosmetic results. So we keep responsive those.

The methodology covers all the customizations into the `custom.scss` file where you can alter every single behavior creating your own `.c-classname` file. It's better this way that to create every single property under a responsive perspective.

If your design on mobile is too radical compared to the desktop, maybe you should use two different UIs with different frontend code than using the same all-in-one code that hammers down the website. The performance gain will be superior.

## Normalizer

Everyone installs [normalizer](https://necolas.github.io/normalize.css/), but few comment on the sections they will never use, therefore, each project already dedicates 6 KB to styles that will never be used. The UCSS framework has a normalizer module, which complies with all normalizer rules, but these are activated according to what you need. To start using it, you need to go to the `config_normalizer` file and start changing the variables to `true` so that it automatically takes effect. No more cost of KBs without impact on the site. You can have your customizer, as I recommend as a philosophy to have the best CSS code: only the classes that are needed.

## Customization

This framework allow you to achieve 99% of your project, but there are some caveats with this way of developing. Classes are wonderful but they don't cover cases like :hover, :focus, etc. You must create those instances in a separate file, name it custom.scss and store those particular behaviors that you cannot cover with the framework.

The way we do it using UCSSM methodology, is to create a custom class. Customs classes in UCSSM are named with a prefix `c-`. Let's imagine you have an image that you want to change opacity when you hover it.

We have found out it is easier to maintain code using this approach. The prefix alerts you from a non-framework behavior, so you can go to only one place to check the class and its properties.

In your template file add a custom class:

<pre>
&lt;img class="display--block opacity--5 c-no-opacity"/&gt;
</pre>

In your `custom.scss` file, define that custom class:

<pre>
.c-no-opacity:hover {
  opacity: 1;
  }
</pre>

Now when you hover that image, it will shift opacity to 1. This just an example on how functional CSS manages changes and interactions. Most of the projects end up with less than 5 lines of custom code.

## List of supported properties

We support all CSS 1, 2 and 3 properties in this framework. You can see extensively each of these properties into our `config_css` file for more information.