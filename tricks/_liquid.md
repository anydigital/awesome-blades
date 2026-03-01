## Liquid <small>Tricks</small>

- https://shopify.github.io/liquid/basics/introduction/
- https://shopify.github.io/liquid/#filters-section

### Syntax highlighting & auto-formatting <sub>in [VS Code~editors](/tricks/antigravity/)</sub> {#liquid-vscode}

1. 🧩 Install https://github.com/prettier/prettier-vscode (if not yet)
2. 🧩 Install https://shopify.dev/docs/storefronts/themes/tools/shopify-liquid-vscode  
   (2-in-1 extension for highlighting & formatting)

This is a huge advantage for `.liquid` over `.njk` so far.

### Prevent unclosed html tags from breaking auto-formatting

`{% # prettier-ignore %}` might not help with that, because the parser crashes on the "broken" HTML before it even reads the ignore command.

But there is a trick with "fake" `{% if true %}` condition:

```liquid {data-caption=_html-begin.liquid}
{% if true %}<html>{% endif %}
<head>
  ...
</head>
{% if true %}<body>{% endif %}
  ...
```

```liquid {data-caption=_html-end.liquid}
{% if true %}</body><html>{% endif %}
```

This "fake conditional" trick is a clever way to bypass the Abstract Syntax Tree (AST) parsers used by formatters like Prettier. Since the formatter sees the tag wrapped in a logic block, it often treats the HTML as a string or a partial fragment rather than a structural error.

### Create array

```liquid {data-caption=.liquid}
{% capture _new_array %}
1
2
3
{% endcapture %}
{% assign _new_array = _new_array | strip | split: '\n' %}
```

### Beware: False Positives <small>in `.liquid`</small>

- https://liquidjs.com/tutorials/truthy-and-falsy.html
- https://www.11ty.dev/docs/languages/liquid/#java-script-truthiness-in-liquid

❌ Wrong:

```liquid
{% if my_string %} This will always show if the string exists, even if empty. {% endif %}
```

✅ Right (Checking for content):

```liquid
{% if my_string != blank %} This only shows if there is actual text. {% endif %}
```

✅ Right (Checking arrays/strings by size):

```liquid
{% if my_array.size > 0 %} This ensures the list isn't empty. {% endif %}
```
