# Wedding Website

[![Build Status](https://travis-ci.org/maruina/maruina.github.io.svg?branch=release)](https://travis-ci.org/maruina/maruina.github.io)

## Installation

1. Install ruby

    ```bash
    brew install ruby

    # Export the new ruby binary
    export PATH=/usr/local/opt/ruby/bin:$PATH

    # Make sure you're using the installed ruby
    which ruby
    # /usr/local/opt/ruby/bin/ruby
    ```

1. Install Jekyll

    ```bash
    gem install --user-install bundler jekyll

    # Get the Ruby version
    ruby -v
    # ruby 2.6.3p62 (2019-04-16 revision 67580) [x86_64-darwin18]

    # Append your path file with the following,
    # replacing the X.X with the first two digits of your Ruby version.
    export PATH=$HOME/.gem/ruby/2.6.0/bin:$PATH
    ```

1. Install required packages

    ```bash
    bundle install
    ```

1. To run the website from the local machine

    ```bash
    bundle exec jekyll serve --future --drafts -l
    ```

## Development

```bash
export PATH=/usr/local/opt/ruby/bin:$PATH
export PATH=$HOME/.gem/ruby/2.6.0/bin:$PATH
bundle exec jekyll serve --future --drafts -l
```

## Components

- To change the background image, replace `images/banner.jpg`
- The index page is based on the `_layouts/landing.html`
- To change the text in the greeting section,
edit `greeting.title` and `greeting.text` in `_config.yml`
**or** edit the `<section id="greeting"` in `_layouts/landing.html`

## Contributing

1. Create your working branch from `release`
1. Open a PR and merge it.
1. Travis will build the website and release it on the `master` branch