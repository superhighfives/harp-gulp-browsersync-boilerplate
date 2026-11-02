# Harp, Gulp, and BrowserSync

A ready-to-go Gulp and Harp setup that injects CSS changes into the page as you save, using BrowserSync.

Status: archived. Made in 2014, not maintained. Harp and Gulp are rarely used for this kind of thing now, and this setup depends on Gulp 3, which doesn't run on current versions of Node. These days a static site generator with a built-in dev server, like Eleventy or Astro, gives you live reloading without the extra wiring.

Write-up: https://github.com/superhighfives/v1.charliegleason.com/blob/master/public/articles/harp-gulp-and-browsersync.md

## How it works

Running `gulp` starts a [Harp](https://harpjs.com) server on port 9000 and puts BrowserSync in front of it as a proxy. Gulp then watches the project:

- Changes to `.css`, `.sass`, `.scss`, or `.less` files are injected into the page without a full reload.
- Changes to `.html`, `.ejs`, `.jade`, `.js`, `.json`, or `.md` files reload the page.

## Getting started

Older versions of Harp could create a new project from this boilerplate:

```shell
harp init src --boilerplate superhighfives/harp-gulp-browsersync-boilerplate
```

Current versions of Harp no longer have `harp init`, so clone the repo instead. Then install the dependencies and start it up:

```shell
npm install
gulp
```

Then, success.
