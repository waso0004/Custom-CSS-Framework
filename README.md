# Frosted CSS Framework

A lightweight, frosted-glass-themed CSS framework built with Sass. It provides sensible base styling for plain HTML elements and optional utility/component classes for customization.

---

## Project To-Do List

### 1) Build the framework with Sass
- [x] Create the CSS Framework using Sass
- [x] Organize it using Sass partials (multiple `.scss` files that get imported into a main file)

### 2) Add customization support
- [x] Use CSS variables or Sass variables so users can customize the framework (colors, spacing, fonts, etc.)

### 3) Create a theme for standard HTML elements
- [x] Headings (`h1` to `h6`)
- [x] Lists (`ul`, `ol`, `li`, `dl`, `dt`, `dd`)
- [x] Buttons (`button`)
- [x] Forms (`form`, `label`, `input`, `textarea`)
- [x] Inputs (text, email, password, textarea, checkbox, radio)
- [x] Tables (`table`, `thead`, `tbody`, `tr`, `th`, `td`)
- [x] Other common base elements (`p`, `a`, `code`, `pre`, `kbd`, `samp`)

### 4) Create utility classes
- [x] Color (text + background)
- [x] Font weight
- [x] Font size
- [x] Margin
- [x] Padding
- [x] Border

### 5) Ensure the theme looks consistent and good
- [x] Apply the theme consistently across all elements
- [x] Make sure everything looks appealing together

### 6) Include the compiled CSS in the repo
- [x] Compile Sass into a final CSS file (`css/frosted.css`)
- [x] Include that compiled output in the repository

### 7) Write the README documentation
- [x] Installation
- [x] Usage
- [x] Customization

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Custom-CSS-Framework.git
   ```

2. Link the compiled CSS in your HTML:
   ```html
   <link rel="stylesheet" href="css/frosted.css" />
   ```

3. (Optional) If you want to modify and recompile the Sass source, install Sass globally:
   ```bash
   npm install -g sass
   ```
   Then compile:
   ```bash
   sass src/frosted.scss css/frosted.css
   ```

---

## Usage

The framework styles plain HTML elements automatically — no classes required for base styling. Just write standard HTML and it works:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="css/frosted.css" />
</head>
<body>
  <h1>Hello World</h1>
  <p>This paragraph is styled automatically.</p>

  <ul>
    <li>Item one</li>
    <li>Item two</li>
  </ul>

  <button>Click Me</button>

  <form>
    <label for="name">Name</label>
    <input type="text" id="name" placeholder="Enter name..." />
    <button type="submit">Submit</button>
  </form>

  <table>
    <thead>
      <tr><th>Name</th><th>Role</th></tr>
    </thead>
    <tbody>
      <tr><td>Alice</td><td>Developer</td></tr>
    </tbody>
  </table>
</body>
</html>
```

### Optional Component Classes

For more control, you can use the included component classes:

| Class | Description |
|---|---|
| `.btn` | Button styling |
| `.btn-primary`, `.btn-success`, `.btn-error` | Button color variants |
| `.form` | Frosted form card wrapper |
| `.form-label`, `.form-control` | Standalone form element classes |
| `.table`, `.table-frosted`, `.table-striped`, `.table-hover` | Table variants |
| `.container`, `.row`, `.col-1` to `.col-12` | Grid layout |

### Utility Classes

| Prefix | Examples | Description |
|---|---|---|
| `.text-{color}` | `.text-blue`, `.text-red` | Text color |
| `.bg-{color}` | `.bg-blue`, `.bg-black` | Background color |
| `.fw-{weight}` | `.fw-bold`, `.fw-light` | Font weight |
| `.fs-{size}` | `.fs-sm`, `.fs-lg` | Font size |
| `.m-{n}`, `.mt-{n}`, `.mx-{n}` | `.m-4`, `.mt-2` | Margin (0–8) |
| `.p-{n}`, `.pt-{n}`, `.px-{n}` | `.p-4`, `.px-2` | Padding (0–8) |
| `.border`, `.border-{n}` | `.border`, `.border-2` | Border width |
| `.rounded`, `.rounded-{size}` | `.rounded`, `.rounded-lg` | Border radius |

---

## Customization

All design tokens are defined as Sass maps in `src/variables/`:

| File | Variables |
|---|---|
| `_colors.scss` | `$colors` (white, black, gray, blue, green, red, purple, pink, yellow), `$theme` (primary, success, error, light, dark) |
| `_typography.scss` | `$fonts` (body, heading, code), `$font-sizes` (sm, md, lg, xl, 2xl, 3xl) |
| `_spacing.scss` | `$spacing` (0–8, from 0 to 64px) |
| `_font-weight.scss` | `$font-weights` (light, regular, medium, bold) |

To customize, edit the variable maps and recompile:

```bash
sass src/frosted.scss css/frosted.css
```

---

## Project Structure

```
src/
├── frosted.scss          # Main entry point
├── index.html            # Demo page (plain HTML)
├── reset/
│   └── _reset.scss       # CSS reset (the-new-css-reset v1.11.3)
├── base/
│   └── _base.scss        # Element-level base defaults
├── variables/
│   ├── _colors.scss      # Color maps
│   ├── _typography.scss   # Font families & sizes
│   ├── _spacing.scss      # Spacing scale
│   ├── _font-weight.scss  # Font weight scale
│   ├── _margin.scss       # Margin variables
│   ├── _padding.scss      # Padding variables
│   └── _border.scss       # Border variables
├── components/
│   ├── _button.scss       # Button mixin & classes
│   ├── _form.scss         # Form mixin & classes
│   ├── _table.scss        # Table classes
│   ├── _heading.scss      # Heading mixin
│   ├── _list.scss         # List mixin
│   ├── _link.scss         # Link mixin
│   ├── _code.scss         # Code/pre mixin
│   └── _grid.scss         # Grid system
├── utilities/
│   ├── _colors.scss       # Color utility classes
│   ├── _font-weight.scss  # Font weight utilities
│   ├── _typography.scss   # Font size utilities
│   ├── _margin.scss       # Margin utilities
│   ├── _padding.scss      # Padding utilities
│   └── _border.scss       # Border utilities
└── fonts/
    ├── _roboto.scss       # Roboto font import
    └── _roboto-mono.scss  # Roboto Mono font import
css/
└── frosted.css            # Compiled output
```