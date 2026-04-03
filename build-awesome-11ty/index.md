---
permalink: /build-awesome-11ty/
title: <sup>Build Awesome /</sup> Eleventy blades
canonical: https://blades.ninja/build-awesome-11ty/
eleventyComputed:
  summary: |-
    {% liquid
      assign _ = 'https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/README.md'
      echo _ | fetch | section: 'summary'
    %}
    https://github.com/anydigital/eleventy-blades ![](https://img.shields.io/github/v/release/anydigital/eleventy-blades?label=&color=black)  
includes:
  - section: docs
    path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/README.md
  - text: |-
      ---
      ## [Templating](/html/)

      {#njk-vscode}
      <!--https://bsky.app/profile/any.digital/post/3mdjvepwr7k2w-->
  - section: toc
    path: https://blades.ninja/html/
  - text: ---
  - path: build-awesome-11ty/_starters.md
  - text: ---
  - section: index
    path: https://raw.githubusercontent.com/anydigital/awesome-11ty-build-awesome/refs/heads/master/README.md

revised: 2026-02-28
---
