# Contributing to [the Freenode #CSS website](http://hashcss.com)

[The Freenode #CSS website](http://hashcss.com) is a resource for all
levels of CSS ability. It is a source of quality [CSS
tutorials](http://hashcss.com/schools) and [CSS
documentation](http://hashcss.com/docs).

# Content Licensing

All content on the website is freely licensed for any use. If you want
to contribute, you must also license your contribution freely. Read the
LICENSE file for details.

# Typos and Broken Links

If you find a typo or a broken link, please [open an issue on the issue
tracker](https://github.com/hashcss/hashcss.com/issues).

# New Links

If you have a new link you'd like to add, fit it into the most
appropriate page:

* [Using #CSS Effectively](http://hashcss.com/using/) is for IRC guides
* [FAQs](http://hashcss.com/faq/) are simple solutions for common issues
* [Tutorials](http://hashcss.com/schools/) are walkthroughs for beginners
* [Docs](http://hashcss.com/docs/) are detailed information for
  intermediate and advanced authors.

# Contributing Content

Currently, the #CSS site is a repository of links to external content.
If you want to contribute content, build your own site ([Github
Pages](http://pages.github.com) is an excellent host) and [open an issue
with your link and the reason you want it
included](https://github.com/hashcss/hashcss.com/issues).

# Forking and Pull Requests

Instead of opening an issue, you can edit the site yourself.

## Jekyll

The #CSS website is built using [Jekyll](http://jekyllrb.com). To get
started:

* Install [Ruby](http://ruby-lang.org)
* Fork and clone this Github repository
* Install the necessary Ruby modules:
    * `gem install bundler`
    * `cd hashcss.com` # The directory containing the cloned repository
    * `bundle install`

The site lives in the src/ directory. To run the site locally:

* cd hashcss.com/src
* jekyll serve --watch

This will serve the site on http://localhost:4000. This will also watch
the site directory for changes and update the site automatically.
