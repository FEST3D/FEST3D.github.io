---
title: Developers
permalink: /docs/home/
redirect_from: /developers/index.html
---

## FEST3D Team

 FEST3D is density-based Navier-Stokes solver and requires a three-dimensional structured grid. For two-dimensional flow, it requires a grid which is, at least, one cell thick in the third direction.
 It uses flux splitting method, either AUSM, LDFSS or SLAU, for constructing inviscid fluxes at faces and Green-Gauss divergence method to calculated cell-based gradients of primitive variables.
 For a more accurate solution, it performs higher order face reconstruction using either MUSCL, PPM or WENO. 
A solution is marched in time using either Euler Explicit, RK2, RK4, TVDRK2, TVDRK3 or TVDRK4 explicit time integration method.
Recently, implicit time integration methodology has been implemented in form of LU-SGS matrix-free method. For turbulent flow, FEST3D has the capability to perform RANS simulation using either SA, SST or k-kL turbulence model. 
FEST3D uses distributed memory based MPI implementation for faster computation using parallel processing. 
FEST3D can write the solution file in two different formats: vtk, and Tecplot.
The good thing about coupling your documentation with the source repo is, whenever you merge features with regarding content to master branch, it will also be published on the webpage instantly.

1. Just [download the source](https://github.com/aksakalli/jekyll-doc-theme/archive/gh-pages.zip) into your repo under `docs` folder.
2. Edit site settings in  `_config.yml` file according to your project. !!! `baseurl` should be your website's relative URI like `/my-proj` !!!
3. Replace `favicon.ico` and `img/logonav.png` with your own logo.

## Writing content

### Docs

Docs are [collections](https://jekyllrb.com/docs/collections/) of pages stored under `_docs` folder. To create a new page:

**1.** Create a new Markdown as `_docs/my-page.md` and write [front matter](https://jekyllrb.com/docs/frontmatter/) & content such as:

```
---
title: My Page
permalink: /docs/my-page/
---

Hello World!
```

**2.** Add the pagename to `_data/docs.yml` file in order to list in docs navigation panel:

```
- title: My Group Title
  docs:
  - my-page
```

### Blog posts

Add a new Markdown file such as `2017-05-09-my-post.md` and write the content similar to other post examples.

### Pages

The homepage is located under `index.html` file. You can change the content or design completely different welcome page for your taste. (You can use [bootstrap components](http://getbootstrap.com/components/))

In order to add a new page, create a new `.html` or `.md` (markdown) file under root directory and link it in `_includes/topnav.html`.
