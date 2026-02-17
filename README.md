# Frosted

A lightweight, class-based CSS framework built with Sass. Frosted gives your UI a frosted glass aesthetic with semi-transparent backgrounds, soft borders, and backdrop blur. All styling is applied through classes, and every design token is driven by Sass variable maps so you can customize colors, spacing, typography, and more.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Custom-CSS-Framework.git
   ```

2. Add the compiled stylesheet to your HTML:
   ```html
   <link rel="stylesheet" href="css/frosted.css" />
   ```

3. If you want to edit the source and recompile, install Sass and run:
   ```bash
   npm install -g sass
   sass src/frosted.scss css/frosted.css
   ```

---

## Usage

Frosted is class-based. Add the provided classes to your HTML elements to apply styles.

### Components

**Headings** use `.h1` through `.h6`:
```html
<h1 class="h1">Page Title</h1>
<h2 class="h2">Section Title</h2>
```

**Buttons** use `.btn` with optional color variants:
```html
<button class="btn">Default</button>
<button class="btn btn-primary">Primary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-error">Error</button>
```

**Forms** can use the `.form` wrapper, which auto-styles child labels, inputs, and selects. You can also use standalone classes like `.form-group`, `.form-label`, `.form-control`, `.form-select`, `.form-check`, `.form-check-input`, and `.form-check-label`:
```html
<form class="form">
  <div class="form-group">
    <label>Email</label>
    <input type="email" placeholder="you@example.com" />
  </div>
  <button class="btn btn-primary" type="submit">Submit</button>
</form>
```

**Tables** use `.table` with optional `.table-frosted`, `.table-striped`, and `.table-hover`:
```html
<table class="table table-frosted table-striped table-hover">
  <thead>
    <tr><th>Name</th><th>Role</th></tr>
  </thead>
  <tbody>
    <tr><td>Alice</td><td>Developer</td></tr>
  </tbody>
</table>
```

**Lists** use `.list` with `.list-item`, `.list-unordered`, `.list-ordered`, `.list-term`, and `.list-detail`.

**Links** use `.link`. **Code** uses `.code`, `.kbd`, `.samp`, and `.pre`.

### Grid

The grid uses `.container`, `.row`, and `.col-1` through `.col-12`. Use `.col` for equal-width columns or `.col-auto` for content-sized columns:
```html
<div class="container">
  <div class="row">
    <div class="col-6">Half</div>
    <div class="col-6">Half</div>
  </div>
</div>
```

### Utility Classes

| Class | Description |
|---|---|
| `.text-{color}` | Text color (e.g. `.text-white`, `.text-blue`) |
| `.bg-{color}` | Background color with frosted glass effect (e.g. `.bg-black`, `.bg-purple`) |
| `.fw-{weight}` | Font weight (e.g. `.fw-bold`, `.fw-light`) |
| `.text-{size}` | Font size (e.g. `.text-sm`, `.text-lg`, `.text-3xl`) |
| `.m-{n}`, `.mt-{n}`, `.mr-{n}`, `.mb-{n}`, `.ml-{n}`, `.mx-{n}`, `.my-{n}` | Margin, 0 to 8 |
| `.p-{n}`, `.pt-{n}`, `.pr-{n}`, `.pb-{n}`, `.pl-{n}`, `.px-{n}`, `.py-{n}` | Padding, 0 to 8 |
| `.border`, `.border-{n}` | Border width |
| `.border-{color}` | Border color |
| `.rounded-{size}` | Border radius (`0`, `sm`, `md`, `full`) |
| `.blur-{n}` | Backdrop blur (0 to 3) |
| `.opacity-{n}` | Opacity |
| `.tracking-{n}` | Letter spacing |
| `.leading-{n}` | Line height (`tight`, `normal`) |
| `.max-w-{size}` | Max width (`sm`, `md`, `lg`) |
| `.mx-auto` | Center horizontally |

---

## Customization

All design tokens live in Sass maps under `src/variables/`. To customize the framework, edit the maps and recompile with `sass src/frosted.scss css/frosted.css`.

**Colors** are defined in `$colors` inside `src/variables/_colors.scss`. To add a new color, add an entry like `'orange': #ffa726` to the map. This generates `.text-orange`, `.bg-orange`, and `.border-orange` utilities automatically.

**Theme colors** are defined in `$theme` in the same file. They map semantic names to color values, for example `'primary': map.get($colors, 'blue')`. To change the primary color, point it to a different value from `$colors` or any hex color.

**Font sizes** are in `$font-sizes` inside `src/variables/_typography.scss`. Each entry like `'lg': 24px` generates a `.text-lg` utility class. Add or change entries to create new sizes.

**Spacing** is in `$spacing` inside `src/variables/_spacing.scss`. The scale runs from `'0': 0` to `'8': 64px` and drives all margin and padding utilities.

**Font weights** are in `$font-weights` inside `src/variables/_font-weight.scss`. Each entry like `'bold': 700` generates a `.fw-bold` utility.

**Border and blur** values are in `src/variables/_border.scss`. The `$border-radius` map controls `.rounded-{size}` classes, and `$blur` controls `.blur-{n}` classes.