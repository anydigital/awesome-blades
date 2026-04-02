---
eleventyNavigation:
  key: <i class="fa-solid fa-picture-in-picture fa-flip-both"></i> Label
  order: 2
title: <a href="/css/">CSS</a> Float Label
eleventyComputed:
  summary: |-
    {% liquid
      assign _ = 'https://raw.githubusercontent.com/anydigital/float-label-css/refs/heads/master/README.md'
      # assign _ = '../../float-label-css/README.md'
      echo _ | fetch | section: 'summary'
    %}
    https://github.com/anydigital/float-label-css from https://github.com/anydigital/blades
includes:
  - section: intro
    path: https://raw.githubusercontent.com/anydigital/float-label-css/refs/heads/master/README.md
    # path: ../../float-label-css/README.md
  - text: |-
      ## Demo

      Drop-in support for **Pico** https://picocss.com/docs/forms :

      <article>
        <form>
          <label>
            <span>Name</span>
            <input placeholder="First Last"/>
          </label>
          <label>
            <span>Bio</span>
            <textarea placeholder="Write a professional short bio..."></textarea>
          </label>
          <label>
            <span>Cuisine</span>
            <select>
              <option selected disabled value="">Select your favorite cuisine...</option>
              <option>Italian</option><option>Japanese</option><option>Indian</option><option>Thai</option><option>French</option>
            </select>
          </label>
          <input type="submit" value="Subscribe"/>
        </form>
      </article>

      More examples:
  - section: docs
    path: https://raw.githubusercontent.com/anydigital/float-label-css/refs/heads/master/README.md
    # path: ../../float-label-css/README.md
  - text: |-
      ---
      ## <sup>PS:</sup> How it works
  - section: code
    path: https://raw.githubusercontent.com/anydigital/blades/refs/heads/main/src/float-label.core.css
---
