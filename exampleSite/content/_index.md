---
title: Bloggraph Example Website
---

{{< figure src="https://desmondlzy.me/bloggraph/teaser.jpg" caption="Welcome to the example website of Bloggraph." >}}

Welcome to the example website of the [Hugo](https://gohugo.io) theme Bloggraph. 
The design of Bloggraph takes lots of inspiration from the style of ACM SIGGRAPH technical paper,
with a special focus on showcasing research projects and profiles.

This website is a minimal example, as well as a tutorial that could get you a quick start.

{{< icon-link >}}

## Start with the Source Code of This Website

The best way to get started is get a copy of the source code of this example website and change it as per your need. 
Simply clone the [github repo](https://github.com/desmondlzy/bloggraph-example) with `--recursive`.
```
git clone --recursive https://github.com/desmondlzy/bloggraph-example yourwebsite
```

Then try `cd yourwebsite; hugo serve` you shall see the example website running at `localhost:1313/`. Make sure you've [installed Hugo extended version](https://gohugo.io/getting-started/installing/) (v0.90.0+) before this.

### Recommended Directory Layout

If you're working with the example website, you're already set. If you are migrating an existing Hugo project, it's highly recommended to organize files as the following:

```
content/
├─ publications/
│  ├─ _index.md (if you want to customize the publication list page)
│  ├─ pequalsnp.md
│  ├─ other-projects.md
├─ _index.md (home page)
static/
├─ sass/
│  ├─ _custom.sass (recommended place to override the default sass)
themes/
├─ bloggraph/
config.toml
```

## Site Configuration

Change the corresponding fields in your [site configuration](https://gohugo.io/getting-started/configuration/#configuration-file) at `config.toml` to customize the following.

### Site Owner Name

Change `name` in `[params.author]`. It will be used to highlight your name in the author list of the publication.

### Social Media Links

Change the fields in `[params.author]`. This determines what <code>{{&lt; icon-link >}}</code> shows.

{{< icon-link >}}

Currently, only `linkedin`, `github` and `email` are supported.
Want more? Tweak `themes/bloggraph/shortcodes/icon-link.html` and file a [pull request](https://github.com/desmondlzy/bloggraph/pulls) to let everyone benefit from it!

### Tabs in the Navigation Bar

Change `[menus.main]`. See [official documentation on menus](https://gohugo.io/content-management/menus) for more info.

## Home Page

Home page (the page shown at the root of your website) is generated from the `content/_index.md`. As usual, use [markdown syntax](https://www.markdownguide.org/) to write things on your home page.


## Publication

Some tools that may come in handy when you write the publication page.


### Add a Publication/Project Page

Set the front matter `type` to be `publications`.
The following command which creates all the boilerplate and front matters will take care of everything.

```
hugo new publications/p-equals-np.md
```

The authors and affiliations information will be parsed from the front matters and displayed on the page automatically.

### Show the Overview of a Publication from Markdown

A [shortcode](https://gohugo.io/content-management/shortcodes) is bundled so that you can refer a publication page in the website by 

<pre><code>{{&lt; publication/single title="Realtime Rendering on a Single Thread" >}}</code></pre> 

{{< publication/single title="Realtime Rendering on a Single Thread" >}}

### Publication List

A list of publication is automatically generated at `baseURL/publications`. You can add customized content before the list at `content/publications/_index.md`.

## Extras

I like snacks...

### Icon Link

Display the your social media links as per the site configuration.

<pre><code>{{&lt; icon-link >}}</code></pre>

{{< icon-link >}}

### Number the Headings/Figures

Use __shortcode__ in the markdown file to number all the h2/h3 headings in the page.
_Note_: `numbering` doesn't work for figure caption.

<pre><code>{{&lt; numbering >}}</code></pre>

Use __HTML class__ `count-figure` and `count-h2h3` if you work with HTML. All the descendants of the container of the corresponding class will have the numbering enabled.