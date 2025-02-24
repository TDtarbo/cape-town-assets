# Import fonts to CSS files

```css
@font-face {
  font-family: "Font-Name";
  src: url("./path/to/file");
}
```

# CSS Variables

```css
:root {
    
  /* Primary Color Variants */
  --color-primary: rgb(0, 0, 0); /* Main brand color */
  --color-primary-light: rgb(51, 51, 51); /* Lighter black */
  --color-primary-dark: rgb(0, 0, 0); /* Stays black */

  /* Secondary Color Variants */
  --color-secondary: rgb(255, 255, 255); /* Supporting color */
  --color-secondary-light: rgb(255, 255, 255); /* Stays white */
  --color-secondary-dark: rgb(230, 230, 230); /* Slightly darker white (light gray) */

  /* Accent Color Variants */
  --color-accent: rgb(127, 127, 127); /* Neutral gray */
  --color-accent-light: rgb(170, 170, 170); /* Lighter gray */
  --color-accent-dark: rgb(85, 85, 85); /* Darker gray */

  /* Font Sizes */
  --font-size-xs: 0.6875rem; /* 11px */
  --font-size-sm: 0.75rem; /* 12px */
  --font-size-m: 0.875rem; /* 14px */
  --font-size-l: 0.9375rem; /* 15px */
  --font-size-xl: 1.5rem; /* 24px */
}
```
