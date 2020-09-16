---
layout: note
title: Common Jekyll Commands
parent: Jekyll
grand_parent: Home
---

# Common Jekyll Commands

The jekyll program has several commands but the structure is always:

```shell
$ jekyll command [argument] [option] [argument_to_option]
```

## Common Commands:

`jekyll new PATH` Creates a new Jekyll site with default gem-based theme at specified path. The directories will be created as necessary.

`jekyll new PATH --blank` Creates a new blank Jekyll site scaffold at specified path.

`jekyll build` or `jekyll b` Performs a one off build your site to ./\_site (by default).

`jekyll serve` or `jekyll s` [[Launch and Run Jekyll Site Locally]].

`jekyll clean` Removes all generated files: destination folder, metadata file, Sass and Jekyll caches.

`jekyll help` Shows help, optionally for a given subcommand, e.g. jekyll help build.

`jekyll new-theme` Creates a new Jekyll theme scaffold.

`jekyll doctor` Outputs any deprecation or configuration issues.

**Typically you’ll use `jekyll serve` while developing locally and `jekyll build` when you need to generate the site for production.**

---
