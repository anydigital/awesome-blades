---
permalink: /jekyll/
title: Jekyll <small>blades</small>
includes:
  - section: jekyll
    path: https://raw.githubusercontent.com/anydigital/blades/refs/heads/main/README.md
---

## Install

All [CSS](https://blades.ninja/css/) and [HTML](https://blades.ninja/html/) blades are available as a Jekyll theme.

<mark>Manually:</mark>

In you `_config.yml`:

```yaml
remote_theme: anydigital/blades@v0.27.0-beta # or latest
plugins:
  - jekyll-remote-theme
```

Living example: https://github.com/anydigital/bladeswitch/blob/main/_config.yml

<mark>Preconfigured:</mark>

[🥷 Bladeswitch Starter ↗ &nbsp;<small style="white-space: nowrap">Jekyll + Pico + Blades</small>](https://github.com/anydigital/bladeswitch)<!--{role=button .outline}-->

---

## Jekyll tricks

### Running GitHub Pages' Jekyll locally

Assuming you already [installed `rbenv`](/random/#rbenv):

1.  ```rb {data-caption=Gemfile}
    source "https://rubygems.org"

    gem "github-pages", group: :jekyll_plugins
    ```

2.  ```sh
    bundle install
    bundle exec jekyll serve
    ```

Living example: https://github.com/anydigital/bladeswitch/blob/main/Gemfile

More info: https://github.com/github/pages-gem#usage, https://jekyllrb.com/docs/installation/macos/
