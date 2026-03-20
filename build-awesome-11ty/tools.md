---
title: <a href="/build-awesome-11ty/">Build Awesome / 11ty</a> Power Tools
includes:
  - section: docs,code
    path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/eleventy.config.js
  - path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/do/README.md
  - text: |-
      ### Find and kill <small>11ty processes</small>

      ```sh
      ps aux | grep eleventy
      pkill -f eleventy
      ```

      You can even combine it with other processes hanging around:

      ```sh
      ps aux | grep -E 'eleventy|tailwind|.bin/serve'
      pkill -f tailwind
      pkill -f .bin/serve
      ```
  - section: docs,code
    path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/siteData.js
---
