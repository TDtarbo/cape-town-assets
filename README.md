# Importing Fonts in CSS

In CSS, you can import custom fonts using `@font-face`.

```css
@font-face {
  font-family: "Font-Name";
  src: url("./path/to/file");
}
```

This allows you to use the custom font throughout your CSS like this:

```css
body {
  font-family: "Font-Name", sans-serif; /*Second one is for fail-safe*/
}
```

---

# CSS Variables

CSS Variables (Custom Properties) allow you to store values like colors, font sizes, and more in a reusable way.

```css
:root {
  /* Primary Colors */
  --color-primary: rgb(0, 0, 0); /* Main brand color */
  --color-primary-light: rgb(51, 51, 51); /* Lighter black */
  --color-primary-dark: rgb(0, 0, 0); /* Stays black */

  /* Secondary Colors */
  --color-secondary: rgb(255, 255, 255); /* Supporting color */
  --color-secondary-light: rgb(255, 255, 255); /* Stays white */
  --color-secondary-dark: rgb(
    230,
    230,
    230
  ); /* Slightly darker white (light gray) */

  /* Accent Colors */
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

To use a CSS variable:

```css
p {
  color: var(--color-primary);
  font-size: var(--font-size-m);
}
```

---

# CSS Pseudo-Classes

A **Pseudo-Class** represents a special state of an element based on user interaction. For example:

```css
button:hover {
  background-color: lightblue;
} /* Changes background when hovered */
```

Common pseudo-classes:

- `:hover` → When a user hovers over an element.
- `:focus` → When an element (like an input field) is focused.
- `:nth-child(n)` → Selects the nth child of a parent.
- `:checked` → Applies styles to checked inputs.

---

# CSS Pseudo-Elements

A **Pseudo-Element** allows you to style specific parts of an element, like text selection or inserting content before/after elements.

```css
input::placeholder {
  color: gray;
  font-style: italic;
} /* Styles the placeholder text */
```

## Common Pseudo-Elements with Examples

### 1. `::before` - Adds content before an element

```css
p::before {
  content: "🔥 ";
}
```

**Output:** 🔥 This is a paragraph.

---

### 2. `::after` - Adds content after an element

```css
p::after {
  content: " 🎉";
}
```

**Output:** This is a paragraph. 🎉

---

### 3. `::first-letter` - Styles the first letter of a paragraph

```css
p::first-letter {
  font-size: 2em;
  color: red;
}
```

**Effect:** The first letter of the paragraph is larger and red.

---

### 4. `::first-line` - Styles the first line of a paragraph

```css
p::first-line {
  font-weight: bold;
  color: blue;
}
```

**Effect:** The first line of the paragraph is bold and blue.

---

### 5. `::selection` - Styles highlighted text

```css
::selection {
  background: yellow;
  color: black;
}
```

**Effect:** Selected text has a yellow background and black text.

---

### 6. `::marker` - Styles bullets/numbers in lists

```css
li::marker {
  color: red;
  font-size: 1.5em;
}
```

**Effect:** Bullets or numbers in lists become red and larger.

---

# Additional Useful Pseudo-Elements

### 7. `::placeholder` - Styles placeholder text inside an `<input>` or `<textarea>`

```css
input::placeholder {
  color: gray;
  font-style: italic;
}
```

✅ Works on `<input>` and `<textarea>` elements.

### 8. `::selection` - Styles highlighted text

```css
::selection {
  background: yellow;
  color: black;
}
```

✅ Works on all text content.

### 9. `::file-selector-button` - Styles file upload buttons

```css
input::file-selector-button {
  background: blue;
  color: white;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
}
```

✅ Works only on `<input type="file">`.

### 10. `::marker` - Styles bullets and numbers in lists

```css
li::marker {
  color: red;
  font-size: 1.5em;
}
```

✅ Works on `<li>` elements inside `<ul>` or `<ol>`.

### 11. `::backdrop` - Styles modal background

```css
dialog::backdrop {
  background: rgba(0, 0, 0, 0.5);
}
```

✅ Works on `<dialog>` elements.
