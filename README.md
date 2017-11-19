# Myst Language Website

This repository contains the source for the Myst programming language home page, (soon to be) available at https://myst-lang.org.


# Development

To run the site locally, simply start up a static webserver within the `docs/` folder. My favorite is the ruby gem `asdf`:

```shell
$ gem install asdf # if you need to
$ cd docs/
$ asdf
```

If you are making changes to the site, you'll need to be running `guard` (another Ruby gem). To help get set up, this project provides a `Gemfile` for Bundler.

```shell
$ gem install bundler # if you don't have bundler installed.
$ bundle # Install dependencies
$ bundle exec guard # start the guard server
```

The source for the website lives in the `src/` folder. This includes the source for the pages and other dynamic content that needs to be compiled. Static assets (CSS, images, etc.) are kept in the `docs/` folder.
