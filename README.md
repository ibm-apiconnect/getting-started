# API Connect Getting Started mini-site

This site is based on the Jekyll theme for [loopback.io](http://loopback.io).
For more information, see [Contributing to LoopBack docs](http://loopback.io/doc/en/contrib/doc-contrib.html).

NOTE: The website is served from the `gh-pages` branch.

## Previewing the site locally

### Setup

Set up Jekyll on your machine:

1. Install [Ruby and Bundler](https://help.github.com/articles/setting-up-your-pages-site-locally-with-jekyll/) if you don't have them already.

1. `cd` to the repository directory and run the following command:

```
$ cd getting-started
$ bundle install
```

Bundler will look in the Gemfile for which gems to install. The `github-pages` gem includes the same version of Jekyll and other dependencies as used by GitHub Pages, so that your local setup mirrors GitHub Pages as closely as possible.

## Run and view site locally

Run Jekyll using the following command:

```
$ bundle exec jekyll serve
```

Then, load [http://localhost:4001/](http://localhost:4001/) on your browser.

## Includes

The site uses several special templates:

### item

Use the `item.md` include to render a markdown string from a YAML file.  It requires one parameter, a YAML property name whose value is the markdown content to display.  
For example, the following displays the content of `create_project.project_pane_open`
in the `microservice.yml` file:

```
{% assign content = site.data.microservice.create_project %}
...
{% include item.md text=content.project_pane_open %}
```

### section-head

Use the `section-head.md` include to display the heading and summary for a section in a YAML file.  It does not accept any parameters, but assumes the `{{content}}` variable has been set to the appropriate YAML property.  For example:

```
{% assign content = site.data.microservice.create_project %}
...
{% include section-head.md %}
```
