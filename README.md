# RJ's Blog

<p align="center" style= "box shadow: 0 0 0 15px rgba(0, 0 ,0, 0.5);" >
  <img src="images/RJ'blog.png"/>
</p>



By default, we use the following:

```css
html {
  font-size: 14px;
  line-height: 1.5;
}
@media (min-width: 38em) {
  html {
    font-size: 20px;
  }
}
## Usage

### 1. Install dependencies

Poole is built on Jekyll and uses its built-in SCSS compiler to generate our CSS. Before getting started, you'll need to install the Jekyll gem:

```bash
$ gem install jekyll
```

**Windows users:** Windows users have a bit more work to do, but luckily [@juthilo](https://github.com/juthilo) has your back with his [Run Jekyll on Windows](https://github.com/juthilo/run-jekyll-on-windows) guide.

**Need syntax highlighting?** *Junior* includes support for Pygments or Rouge, so install your gem of choice to make use of the built-in styling. Read more about this [in the Jekyll docs](http://jekyllrb.com/docs/templates/#code_snippet_highlighting).

### 2a. Quick start

To help anyone with any level of familiarity with Jekyll quickly get started, *Junior* includes everything you need for a basic Jekyll site. To that end, just download *Junior* and start up Jekyll.

### 2b. Roll your own Jekyll site

Folks wishing to use Jekyll's templates and styles can do so with a little bit of manual labor. Download *Junior* and then copy what you need (likely `_layouts/`, `*.html` files, `atom.xml` for RSS, and `public/` for CSS, JS, etc.).

### 3. Running locally

To see your Jekyll site with *Junior* applied, start a Jekyll server. In Terminal, from `/junior-theme` (or whatever your Jekyll site's root directory is named):

```bash
> jekyll serve # You might need "bundle exec jekyll serve"
```
Open <http://localhost:4000> in your browser, and voilà.

## License

Open sourced under the [MIT license](LICENSE).

<3
hello everyone
