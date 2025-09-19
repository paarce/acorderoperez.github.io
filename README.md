# Augusto Cordero Pérez - Senior iOS Tech Lead Portfolio

Professional portfolio website showcasing 12+ years of iOS development expertise, specializing in FinTech solutions and technical leadership. Built with Jekyll and optimized for both technical recruiters and hiring managers.

🌐 **Live Site:** [acorderoperez.github.io](https://acorderoperez.github.io)

## About This Portfolio

This site serves as a comprehensive showcase of my professional journey as a Senior iOS Tech Lead, highlighting:

- **Technical Leadership:** Leading cross-functional teams in complex FinTech projects
- **FinTech Expertise:** Architecting secure payment solutions for major banks
- **International Impact:** Delivering products serving users across Spain, Germany, and Latin America
- **Modern iOS Development:** Swift, SwiftUI, Clean Architecture, CI/CD pipelines

## Portfolio Highlights

### Featured Projects
- **Openbank - Zinia FinTech Platform** (2023): Led iOS development for innovative installment payment solution
- **Xing Professional Network** (2021): Enhanced networking features for millions of European users
- **Additional Projects:** Retail, Immersive Technologies, and FinTech solutions

### Key Achievements
- 12+ years iOS development experience
- Led teams of 5-8 developers across multiple high-impact projects
- Early adopter of SwiftUI, Async/Await, and modern iOS technologies
- Implemented clean architecture patterns and accessibility standards

## Multilingual Support

The portfolio is available in both English and Spanish:
- **English:** Main pages optimized for international opportunities
- **Spanish:** `about-es.html` and `_data/sidebar-es.yml` for Spanish-speaking markets

*Based on the Treat Jekyll template by [CloudCannon](http://cloudcannon.com/)*

## Features

* Contact form
* Pre-built pages
* Pre-styled components
* Blog with pagination
* Disqus comments for posts
* Configurable sidebar
* Optimised for editing in [CloudCannon](http://cloudcannon.com/)
* RSS/Atom feed
* SEO tags
* Google Analytics

## Setup

1. Add your site and author details in `_config.yml`.
2. Add your Google Analytics, Disqus and MailChimp keys to `_config.yml`.
3. Add your details to `_data/sidebar.yml`
4. Get a workflow going to see your site's output (with [CloudCannon](https://app.cloudcannon.com/) or Jekyll locally).

## Develop

Treat was built with [Jekyll](http://jekyllrb.com/) version 3.4.3, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

Treat is already optimised for adding, updating and removing recipes, navigation, page content, and sidebar information in CloudCannon.

### Posts/Recipes

* Add, update or remove a post in the *Posts* collection.
* The recipes page is organised by categories.
* Change the defaults when new posts are created in `_posts/_defaults.md`.

### Contact Form

* Preconfigured to work with CloudCannon, but easily changed to another provider (e.g. [FormSpree](https://formspree.io/)).
* Sends email to the address listed in company details.

### Navigation

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Navigation* section.

### Footer

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Footer* section.

## Error

```bash
`require': cannot load such file -- webrick (LoadError)
```
Solution: https://github.com/jekyll/jekyll/issues/8523