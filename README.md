# Bloggraph

An academic theme for [Hugo](https://gohugo.io/), in the style of SIGGRAPH technical paper. Computer graphics people, you know what it is ;)

## Install

Follow the "[Add a theme](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme)" section in the official [quick start guide](https://gohugo.io/getting-started/quick-start).

```
cd yourwebsiteroot
git init
git submodule add https://github.com/desmondlzy/bloggraph.git themes/bloggraph
```

Set the theme to `bloggraph` in your site config file (`config.toml`/`config.yaml`/`config.json`).

## Usage

The theme is geared towards researchers to showcase their research-related information. Important features include:

- _Home page template_ for showing basic information and publications
- _Publication page template_ for a SIGGRAPH-style research project page

It's recommended to start with the example website (`exampleSite/` in this repo).

### Recommended Directory Layout

```
content/
├─ publications/
│  ├─ pequalsnp.md
│  ├─ other-projects.md
├─ _profile.md (bio and social media links; see notes below)
├─ _index.md (home page)
static/
├─ sass/
│  ├─ _custom.sass (recommended place to override the default sass)
themes/
├─ bloggraph/
├─ otherthemes/
config.toml
```

### Profile on Home Page
```
---
github: desmondlzy
linkedin: desmondlzy
email: zhenyuan.liu [at] ist.ac.at
avatar:
  src: images/photo.jpg
  caption: In Hong Kong, 2019
---
I am a research intern at [IST Austria](https://ist.ac.at),
advised by [Prof. Bernd Bickel](https://berndbickel.com/about-me).
I graduated from [CUHK](https://cuhk.edu.hk) with a BSc. in Computer Science (first class honors) in July 2021.

I enjoy exploring colors and shapes in both physical and virtual worlds (and in their intersection).
Check my [resume](./cv.pdf) for more information.
```


### New Publication

```
hugo new publications/p-equals-np.md
```
The above command creates a template with all front matters and boilerplate code. Recommended as a handyy starting point for a new publication page.

### Shortcodes

- `numbering`: Automatic number all the `<figure>`/`<h2>`/`<h3>` HTML tags in the current document.
	- param: h2=true/false (default: true), number h2 tags;
	- param: h3=true/false (default: true), number h3 tags;
	- param: figure=true/false (default: true), number the figures;
- `publication/single`: show a preview of a publication of a given title.
	- param: title="", use to match the publication to show, must be identical to the `title` field in the front matter of the corresponding markdown file.
- `publication/list`:  show list of preview of all publications.
	- no parameter.

## Credits

The design is inspired by the ACM SIGGRAPH technical paper template. Part of the CSS and template files are modified from the theme [Newsroom](https://github.com/onweru/newsroom).

The following fonts are bundled with `bloggraph` (click for license):
[FontAwesome](https://fontawesome.com/v4.7/license/), 
[Linux Biolinum](https://www.fontsquirrel.com/license/linux-biolinum), and 
[Linux Libertine](https://www.fontsquirrel.com/license/linux-libertine).