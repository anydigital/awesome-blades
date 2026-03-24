---
title: <a href="/build-awesome-11ty/">Build Awesome / 11ty</a> Power Tools
includes:
  - text: |-
      ## Blades starters {#starters}
      <nav class="grid">

      ### [🥷 Build Awesome Starter ↗ <br><small>11ty ⁺ Tailwind ⁺ Typography ⁺ Blades</small>](https://github.com/anydigital/build-awesome-starter){role=button .outline}
      ### [🥷 Bladeswitch Starter ↗ <br><small>Jekyll ⁺ Pico ⁺ Blades</small>](https://github.com/anydigital/bladeswitch){role=button .outline}
      </nav>
      <hr>
  - section: docs,code
    path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/eleventy.config.js
  - path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/do/README.md
  - section: docs,code
    path: https://raw.githubusercontent.com/anydigital/eleventy-blades/refs/heads/main/src/siteData.js
  - text: |-
      ### Appendix
      #### Find and kill <small>11ty processes</small>

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
---
