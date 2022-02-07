# Bloggraph

![Bloggraph Teaser](https://github.com/desmondlzy/bloggraph-example/blob/main/content/teaser.jpg)

An academic theme for [Hugo](https://gohugo.io/), in the style of SIGGRAPH paper. Computer graphics people, you know what it is ;)

See [example website](https://desmondlzy.me/bloggraph) and my [personal website](https://desmondlzy.me) (which uses a tweaked version of the theme).

## Install

If you want to start a new website with Bloggraph, following the [example website](https://desmondlzy.me/bloggraph) is the easiest way to get started.

Alternatively,

Follow the "[Add a theme](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme)" section in the official [quick start guide](https://gohugo.io/getting-started/quick-start).

```
cd yourwebsiteroot
git init
git submodule add https://github.com/desmondlzy/bloggraph.git themes/bloggraph
```

Set the `theme` to `bloggraph` in your site config file (`config.toml`/`config.yaml`/`config.json`).

## Usage

The theme is geared towards researchers who intend to showcase their research profile. Important features include:

- _Home page template_ for showing basic information and publications
- _Publication page template_ for a SIGGRAPH-style research project page
- _Shortcode for numbering figure_

### More details on the example website

For usage and a starting boilerplate, check out the [example website](https://desmondlzy.me/bloggraph).

## Credits

The design is inspired by the ACM SIGGRAPH technical paper template. Part of the CSS and template files are modified from the theme [Newsroom](https://github.com/onweru/newsroom).

The following fonts are bundled with Bloggraph:
[FontAwesome](https://fontawesome.com/v4.7/license/), 
[Linux Biolinum](https://www.fontsquirrel.com/license/linux-biolinum), and 
[Linux Libertine](https://www.fontsquirrel.com/license/linux-libertine).