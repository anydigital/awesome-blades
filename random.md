---
title: Random <small>tricks</small>
canonical: https://blades.ninja/random/
---

## Google Sheets

|                       |                 |
| --------------------- | --------------- |
| <code>Ctrl + `</code> | toggle formulas |

---

## Google Chrome

### chrome://settings/syncSetup/advanced

Customize sync:

- History OFF
- Tabs OFF
- Pwds OFF
- Addresses OFF
- Payments OFF

Rely on Password Manager better.

---

## Terminal

### Check HTTP headers with `curl`

```sh
curl --head HTTP_URL

# or simply:
curl -I HTTP_URL
```

The `-I` flag (shorthand for `--head`) fetches only the HTTP headers from a server. This is the fastest way to inspect status codes, content types, and server metadata without downloading the actual page content.

---

## Regular Expressions {#regex}

Find all lines ending with `**`:

```
\*\*$\n
```

---

## Ruby

Run Ruby projects locally on macOS without breaking system's Ruby:

### Install `rbenv` {#rbenv}

Assuming you already have Homebrew:

```sh
brew install rbenv

# Then list available Ruby versions, and install one:
rbenv install -l
rbenv install 3.2.10

# Set it for current project/folder:
rbenv local 3.2.10
```

Finally, add it to your shell's configuration file so it executes automatically:

```{data-caption=~/.zshrc}
eval "$(rbenv init -)"
```

### GitHub Pages' Jekyll locally

Assuming you already [installed `rbenv`](#rbenv):

1. ```rb {data-caption=Gemfile}
   source "https://rubygems.org"

   gem "github-pages", group: :jekyll_plugins
   ```

2. ```sh
   bundle install
   bundle exec jekyll serve
   ```

More info: https://github.com/github/pages-gem#usage, https://jekyllrb.com/docs/installation/macos/

### Slate Docs locally

Assuming you already [installed `rbenv`](#rbenv):

```sh
bundle install
bundle exec middleman build
```

> For the official version of Slate (v2.13.1), the best and most stable Ruby version is Ruby 3.1.
> While older documentation mentions Ruby 2.6 or 2.7, Slate officially dropped support for Ruby 2.5 and added formal support for Ruby 3.1 in its 2022 releases. Newer versions of Ruby (3.2+) can sometimes cause dependency conflicts with Slate's core engine, middleman, specifically regarding the nokogiri gem.

More info: https://github.com/slatedocs/slate/wiki/Using-Slate-Natively#installing-dependencies-on-macos

---

## Discord

### How to Link a Channel Across Different Servers (Advanced)

To link a channel from Server A into a message in Server B, you need the Channel ID:

1. Enable Developer Mode: Go to User Settings > Advanced and toggle on Developer Mode.
2. Copy ID: Right-click the channel name (or long-press on mobile) and select Copy Channel ID.
3. Use this Syntax: In your message, type `<#CHANNEL_ID>` (replacing CHANNEL_ID with the numbers you copied).
