# W3C Design Tokens using Style Dictionary

## Overview

This is a sample project showing how to use Design Tokens in the [W3C (DTCG) format](https://tr.designtokens.org/format) with [Style Dictionary](https://amzn.github.io/style-dictionary) and [Style Dictionary Utils](https://github.com/lukasoppermann/style-dictionary-utils).

Take your design tokens that look like this:

```json
{
  "color": {
    "violet": {
      "$type": "color",
      "$value": "#7c3aed"
    },
    "rose": {
      "$type": "color",
      "$value": "#e11d48"
    },
    "primary": {
      "$type": "color",
      "$value": "{color.violet}"
    },
    "secondary": {
      "$type": "color",
      "$value": "{color.rose}"
    }
  },
  "fontSize": {
    "small": {
      "$type": "dimension",
      "$value": "12px"
    },
    "medium": {
      "$type": "dimension",
      "$value": "16px"
    },
    "large": {
      "$type": "dimension",
      "$value": "24px"
    }
  },
  "fontWeight": {
    "light": {
      "$type": "fontWeight",
      "$value": 300
    },
    "normal": {
      "$type": "fontWeight",
      "$value": 400
    },
    "bold": {
      "$type": "fontWeight",
      "$value": 600
    }
  },
  "spacing": {
    "small": {
      "$type": "dimension",
      "$value": "12px"
    },
    "medium": {
      "$type": "dimension",
      "$value": "16px"
    },
    "large": {
      "$type": "dimension",
      "$value": "20px"
    }
  }
}
```

And turn them into CSS that looks like this:

```css
:root {
  --font-weight-bold: 600;
  --font-weight-normal: 400;
  --font-weight-light: 300;
  --font-size-large: 1.5rem;
  --font-size-medium: 1rem;
  --font-size-small: 0.75rem;
  --spacing-large: 1.25rem;
  --spacing-medium: 1rem;
  --spacing-small: 0.75rem;
  --color-rose: rgba(225, 29, 72, 1);
  --color-violet: rgba(124, 58, 237, 1);
  --color-secondary: var(--color-rose);
  --color-primary: var(--color-violet);
}
```

See the [video tutorial](https://youtu.be/RcxP0RePlVU) for full details.

## Author

[Mykhaylo Ryechkin](https://github.com/mryechkin)

## License

[MIT](https://choosealicense.com/licenses/mit/)
