# Webworke.rs
**Life and Craft in Columbus, Ohio**

Webworke.rs runs on [Jekyll](http://jekyllrb.com/), a blog-aware, static site generator, with some help from [Grunt](http://gruntjs.com/).

## The Stack
- [Node.js](http://nodejs.org/) and [NPM](https://npmjs.org/): Required for Grunt and Bower
- [Ruby](http://www.ruby-lang.org/): Required for Jekyll and Sass
- [Bower](http://bower.io/): Manage most (but not all) of the front-end dependencies
- [Bundler](http://gembundler.com/): Manage Ruby dependencies
- [Grunt](http://gruntjs.com/): Automate Jekyll development and build tasks
- [ImageMagick](http://www.imagemagick.org/script/): For [Jekyll Picture Tag](https://github.com/robwierzbowski/jekyll-picture-tag).

### Recommended Setup
- Ensure that [Command Line Tools for Xcode](https://developer.apple.com/xcode/) is installed and up-to-date
    - To install: `xcode-select --install`
- Manage your Ruby enviroments with [RVM](https://rvm.io/) or [rbenv](https://github.com/sstephenson/rbenv)
    - To update RVM : `rvm get stable`
- Use [Homebrew](http://brew.sh/) to manage [Node.js](http://nodejs.org/) and [ImageMagick](http://www.imagemagick.org/script/)
    - To install Homebrew: `ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"`
    - To install Node.js: `brew install node`
    - To install ImageMagick:`brew install imagemagick`
    - To update: `brew update`
    - To upgrade: `brew upgrade`
    - To cleanup: `brew cleanup`
    - To check for known issues: `brew doctor`
- Install the command line interface for Grunt (please note that Grunt is actually managed by NPM)
    - To install: `npm install -g grunt-cli`
- Install Bower
    - To install: `npm install -g bower`

## Install Dependencies
Run the following commands to install the dependencies:
- NPM: `npm cache clean` and then `npm install`
- Bundler: `bundle`
- Bower: `bower install`

## Grunt Workflow
- `grunt serve`: Compiles all files and opens the site in your default browser. A watch task watches for changes to files, recompiles if necessary, and injects the changes into the browser with LiveReload
- `grunt check`: Checks for outdated dependencies with grunt-dev-update, Javascript code quality with JSHint, and Jekyll health with `jekyll doctor`
- `grunt build`: Builds an optimized site to the dist directory
- `grunt deploy`: Builds an optimized site to the dist directory and then deploys it.

## Hat Tip
The site was scaffolded by [Yeoman](http://yeoman.io/) and [generator-jekyllrb](https://github.com/robwierzbowski/generator-jekyllrb), the latter being a project of [@robwierzbowski](https://github.com/robwierzbowski). Learn more about the site by reading the [Colophon](http://webworke.rs/colophon/).
