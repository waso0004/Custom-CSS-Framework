# Frosted

A lightweight, class-based CSS framework built with Sass. Frosted gives your UI a frosted glass look using semi-transparent backgrounds, soft borders, and backdrop blur. All styling is applied through classes, and every design token is driven by Sass variable maps for easy customization.

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

Frosted is class-based. Apply the provided classes to your HTML elements to style them.

### Headings

Use `.h1` through `.h6` to style heading elements:

```html
<h1 class="h1">Page Title</h1>
<h2 class="h2">Section Title</h2>
<h3 class="h3">Subsection</h3>
<h4 class="h4">Small Heading</h4>
<h5 class="h5">Smaller Heading</h5>
<h6 class="h6">Smallest Heading</h6>
```

| Class | Description |
|---|---|
| `.h1` | Heading size 2.5rem |
| `.h2` | Heading size 2rem |
| `.h3` | Heading size 1.75rem |
| `.h4` | Heading size 1.5rem |
| `.h5` | Heading size 1.25rem |
| `.h6` | Heading size 1rem |

### Buttons

Use `.btn` for the default button style. Add `.btn-primary`, `.btn-success`, or `.btn-error` for color variants:

```html
<button class="btn">Default</button>
<button class="btn btn-primary">Primary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-error">Error</button>
```

| Class | Description |
|---|---|
| `.btn` | Default frosted button |
| `.btn-primary` | Blue background variant |
| `.btn-success` | Green background variant |
| `.btn-error` | Red background variant |

### Forms

The `.form` wrapper auto-styles child labels, inputs, textareas, and selects. Checkboxes and radios keep their native appearance. Use `.form-group` to group a label and input together:

```html
<form class="form">
  <div class="form-group">
    <label>Email</label>
    <input type="email" placeholder="you@example.com" />
  </div>
  <div class="form-group">
    <label>Password</label>
    <input type="password" placeholder="Enter password..." />
  </div>
  <div class="form-group">
    <label>Message</label>
    <textarea placeholder="Write something..."></textarea>
  </div>
  <div class="form-group">
    <label>Role</label>
    <select>
      <option>Developer</option>
      <option>Designer</option>
    </select>
  </div>
  <div class="form-check">
    <input class="form-check-input" type="checkbox" id="terms" />
    <label class="form-check-label" for="terms">I agree</label>
  </div>
  <div class="form-check">
    <input class="form-check-input" type="radio" name="plan" id="free" />
    <label class="form-check-label" for="free">Free</label>
  </div>
  <button class="btn btn-primary" type="submit">Submit</button>
</form>
```

You can also use standalone classes outside the `.form` wrapper:

| Class | Description |
|---|---|
| `.form-group` | Groups a label and input with bottom margin |
| `.form-label` | Styles a label |
| `.form-control` | Styles a text input or textarea |
| `.form-select` | Styles a select dropdown |
| `.form-check` | Wraps a checkbox or radio with its label |
| `.form-check-input` | Styles a checkbox or radio input |
| `.form-check-label` | Styles the label next to a checkbox or radio |

### Tables

Use `.table` for base table styling. Add `.table-frosted` for the glass effect, `.table-striped` for alternating row backgrounds, and `.table-hover` for hover highlights:

```html
<table class="table table-frosted table-striped table-hover">
  <thead>
    <tr><th>Name</th><th>Role</th></tr>
  </thead>
  <tbody>
    <tr><td>Alice</td><td>Developer</td></tr>
    <tr><td>Bob</td><td>Designer</td></tr>
  </tbody>
</table>
```

| Class | Description |
|---|---|
| `.table` | Base table styling with spacing and borders |
| `.table-frosted` | Adds frosted glass background and border |
| `.table-striped` | Alternating row background colors |
| `.table-hover` | Highlight rows on hover |

### Lists

Use `.list` as the base, then add a type class and `.list-item` for each entry:

```html
<ul class="list list-unordered">
  <li class="list-item">First item</li>
  <li class="list-item">Second item</li>
</ul>

<ol class="list list-ordered">
  <li class="list-item">Step one</li>
  <li class="list-item">Step two</li>
</ol>

<dl class="list">
  <dt class="list-term">Term</dt>
  <dd class="list-detail">Definition of the term</dd>
</dl>
```

| Class | Description |
|---|---|
| `.list` | Base list styling |
| `.list-item` | Styles a list item |
| `.list-unordered` | Disc bullet style |
| `.list-ordered` | Decimal numbered style |
| `.list-term` | Bold term in a definition list |
| `.list-detail` | Definition text in a definition list |

### Links

Use `.link` to style anchor elements:

```html
<a class="link" href="#">Read more</a>
```

| Class | Description |
|---|---|
| `.link` | Blue underlined link with hover opacity |

### Code

Use `.code`, `.kbd`, and `.samp` for inline code elements. Use `.pre` for code blocks. When `.code` is nested inside `.pre`, its background and border are removed automatically:

```html
<p>Run <code class="code">npm install</code> to get started.</p>
<p>Press <kbd class="kbd">Ctrl + C</kbd> to copy.</p>

<pre class="pre"><code class="code">const x = 42;
console.log(x);</code></pre>
```

| Class | Description |
|---|---|
| `.code` | Inline code with frosted background |
| `.kbd` | Keyboard input styling |
| `.samp` | Sample output styling |
| `.pre` | Preformatted code block with backdrop blur |

### Grid

Use `.container`, `.row`, and `.col-1` through `.col-12` for a 12-column layout. Columns stack to full width below 768px. Use `.col` for equal-width columns or `.col-auto` for content-sized columns:

```html
<div class="container">
  <div class="row">
    <div class="col-6">Half</div>
    <div class="col-6">Half</div>
  </div>
  <div class="row">
    <div class="col">Equal</div>
    <div class="col">Equal</div>
    <div class="col">Equal</div>
  </div>
  <div class="row">
    <div class="col-auto">Fits content</div>
    <div class="col">Takes remaining space</div>
  </div>
</div>
```

| Class | Description |
|---|---|
| `.container` | Centered wrapper with max width 1200px |
| `.row` | Flex container for columns |
| `.col-1` to `.col-12` | Fixed-width column (1/12 to 12/12) |
| `.col` | Equal-width flexible column |
| `.col-auto` | Column sized to its content |

### Utility Classes

#### Color

| Class | Description |
|---|---|
| `.text-{color}` | Sets text color. Available colors: `white`, `black`, `gray`, `blue`, `green`, `red`, `purple`, `pink`, `yellow` |
| `.bg-{color}` | Sets a semi-transparent background with backdrop blur. Same color options as above |

#### Typography

| Class | Description |
|---|---|
| `.text-{size}` | Sets font size. Sizes: `sm` (12px), `base` (14px), `md` (16px), `lg` (24px), `xl` (36px), `2xl` (48px), `3xl` (64px) |
| `.fw-{weight}` | Sets font weight. Weights: `light` (300), `regular` (400), `medium` (500), `bold` (700) |
| `.tracking-{n}` | Sets letter spacing. Values: `0` (0), `1` (1px), `2` (2px) |
| `.leading-{n}` | Sets line height. Values: `tight` (1.2), `normal` (1.5) |
| `.max-w-{size}` | Sets max width. Sizes: `sm` (50%), `md` (800px), `lg` (1200px) |

#### Spacing

Margin and padding utilities use a scale from `0` to `8` (0px, 4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px).

| Class | Description |
|---|---|
| `.m-{n}` | Margin on all sides |
| `.mt-{n}`, `.mr-{n}`, `.mb-{n}`, `.ml-{n}` | Margin on a single side |
| `.mx-{n}` | Horizontal margin |
| `.my-{n}` | Vertical margin |
| `.mx-auto` | Centers an element horizontally |
| `.p-{n}` | Padding on all sides |
| `.pt-{n}`, `.pr-{n}`, `.pb-{n}`, `.pl-{n}` | Padding on a single side |
| `.px-{n}` | Horizontal padding |
| `.py-{n}` | Vertical padding |

#### Border

| Class | Description |
|---|---|
| `.border` | Adds a 1px solid border |
| `.border-{n}` | Sets border width. Values: `0`, `1` (1px), `2` (2px), `3` (3px), `4` (4px) |
| `.border-none` | Removes the border |
| `.border-{color}` | Sets border color. Same color options as `.text-{color}` |
| `.rounded-{size}` | Sets border radius. Sizes: `0` (0), `sm` (8px), `md` (20px), `full` (9999px) |

#### Effects

| Class | Description |
|---|---|
| `.blur-{n}` | Sets backdrop blur. Values: `0` (0px), `1` (2px), `2` (4px), `3` (8px) |
| `.opacity-{n}` | Sets opacity. Values: `0`, `2`, `4`, `5`, `8`, `10`, `15`, `20`, `30`, `40`, `75`, `80`, `90`, `100` |

---

## Customization

All design tokens live in Sass maps under `src/variables/`. Edit the maps and recompile with `sass src/frosted.scss css/frosted.css` to apply your changes. Adding or removing entries from a map automatically updates the generated classes.

### Colors

Defined in `$colors` inside `src/variables/_colors.scss`. Each entry generates `.text-{name}`, `.bg-{name}`, and `.border-{name}` utilities. To add a color, insert a new entry like `'orange': #ffa726`.

### Theme Colors

Defined in `$theme` inside `src/variables/_colors.scss`. These map semantic names to values from `$colors` and are used by button variants. For example, `'primary': map.get($colors, 'blue')` controls `.btn-primary`. Change it to any color value.

### Opacity

Defined in `$opacity` inside `src/variables/_colors.scss`. Each entry generates an `.opacity-{n}` utility class. The values are also used internally for semi-transparent backgrounds and borders across all components.

### Font Families

Defined in `$fonts` inside `src/variables/_typography.scss`. The map has three keys: `'body'` for general text, `'heading'` for headings, and `'code'` for code elements. Change any value to use a different font family.

### Font Sizes

Defined in `$font-sizes` inside `src/variables/_typography.scss`. Each entry generates a `.text-{name}` utility. The map includes general sizes (`sm`, `base`, `md`, `lg`, `xl`, `2xl`, `3xl`) and heading sizes (`h1` through `h6`).

### Letter Spacing

Defined in `$letter-spacing` inside `src/variables/_typography.scss`. Each entry generates a `.tracking-{n}` utility.

### Line Height

Defined in `$line-height` inside `src/variables/_typography.scss`. Each entry generates a `.leading-{name}` utility.

### Max Widths

Defined in `$max-widths` inside `src/variables/_typography.scss`. Each entry generates a `.max-w-{name}` utility. The `lg` value also controls the `.container` max width.

### Breakpoints

Defined in `$breakpoints` inside `src/variables/_typography.scss`. The `md` breakpoint (768px) is used by the grid to stack columns on smaller screens.

### Spacing

Defined in `$spacing` inside `src/variables/_spacing.scss`. The scale runs from `'0': 0` to `'8': 64px` and drives all margin and padding utility classes.

### Margin

Defined in `$margin` inside `src/variables/_margin.scss`. Uses the same scale as spacing and is referenced by components for internal margin values.

### Padding

Defined in `$padding` inside `src/variables/_padding.scss`. Uses the same scale as spacing and is referenced by components for internal padding values.

### Font Weights

Defined in `$font-weights` inside `src/variables/_font-weight.scss`. Each entry generates a `.fw-{name}` utility. Default values: `'light': 300`, `'regular': 400`, `'medium': 500`, `'bold': 700`.

### Border Widths

Defined in `$border-widths` inside `src/variables/_border.scss`. Each entry generates a `.border-{n}` utility.

### Border Radius

Defined in `$border-radius` inside `src/variables/_border.scss`. Each entry generates a `.rounded-{name}` utility. Also used by components for their default border radius.

### Blur

Defined in `$blur` inside `src/variables/_border.scss`. Each entry generates a `.blur-{n}` utility. The `'1'` value (2px) is the default blur used across all frosted glass components.