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
</pre>


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