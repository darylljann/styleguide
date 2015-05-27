# CSS guidelines

The following document outlines a how developers at finder.com.au write CSS to ensure all work is reliable and consistent.

We are inspired by projects like [Idiomatic CSS](https://github.com/necolas/idiomatic-css) and [CSS Guidelines](http://cssguidelin.es/) and [BEM](https://en.bem.info/).

This is a living document and new ideas are always welcome. Please contribute.

## Table of contents

1. [General principles](#general-principles)
2. [Whitespace](#whitespace)
3. [Comments](#comments)
4. [Format](#format)
5. [Vendor Prefixes](#vendor-prefixes)
6. [Naming convensions](#naming-convensions)
7. [Validating CSS](#validating-css)
8. [Practical example](#example)

<a name="general-principles"></a>
## 1. General principles

* Don't try to prematurely optimize your code; keep it readable and
  understandable.
* All code in any code-base should look like a single person typed it, even
  when many people are contributing to it.
* If in doubt when deciding upon a style use existing, common patterns (e.g. Media Object).
* If you have multiple style sheets, you must combine and minify them into one to improve performance and reduce additional http requests.
* All code names, descriptions and comments must be in English.

<a name="whitespace"></a>
## 2. Whitespace

Only one style should exist across the entire source of your code-base. Always
be consistent in your use of whitespace. Use whitespace to improve
readability.

* Indent using 2 spaces
* _Never_ mix spaces and tabs for indentation.

Tip: configure your editor to "show invisibles" or to automatically remove
end-of-line whitespace.

Tip: use an [EditorConfig](http://editorconfig.org/) file (or equivalent) to
help maintain the basic whitespace conventions that have been agreed for your
code-base.


<a name="comments"></a>
## 3. Comments

Well commented code is extremely important. Take time to describe components,
how they work, their limitations, and the way they are constructed. Don't leave
others in the team guessing as to the purpose of uncommon or non-obvious
code.

Comment style should be simple and consistent within a single code base.

* Place comments on a new line above their subject.
* Keep line-length to a sensible maximum, e.g., 80 columns.
* Make liberal use of comments to break CSS code into discrete sections.
* Use "sentence case" comments and consistent text indentation.

Tip: configure your editor to provide you with shortcuts to output agreed-upon
comment patterns.

Example:

```css
/* ==========================================================================
   Section comment block
   ========================================================================== */

/* Sub-section comment block
   ========================================================================== */

/**
 * Short description using Doxygen-style comment format
 *
 * The first sentence of the long description starts here and continues on this
 * line for a while finally concluding here at the end of this paragraph.
 *
 * The long description is ideal for more detailed explanations and
 * documentation. It can include example HTML, URLs, or any other information
 * that is deemed necessary or useful.
 *
 * @tag This is a tag named 'tag'
 *
 * TODO: This is a todo statement that describes an atomic task to be completed
 *   at a later date. It wraps after 80 characters and following lines are
 *   indented by 2 spaces.
 */

/* Basic comment */
```




<a name="format"></a>
## 4. Format

The chosen code format must ensure that code is: easy to read; easy to clearly
comment; minimizes the chance of accidentally introducing errors; and results
in useful diffs and blames.

* Use one discrete selector per line in multi-selector rulesets.
* Include a single space before the opening brace of a ruleset.
* Include one declaration per line in a declaration block.
* Use one level of indentation for each declaration.
* Include a single space after the colon of a declaration.
* Use lowercase and shorthand hex values, e.g., `#aaa`.
* Use single or double quotes consistently. Preference is for single quotes,
  e.g., `content: ''`.
* Quote attribute values in selectors, e.g., `input[type='checkbox']`.
* _Where allowed_, avoid specifying units for zero-values, e.g., `margin: 0`.
* Include a space after each comma in comma-separated property or function
  values.
* Include a semi-colon at the end of the last declaration in a declaration
  block.
* Place the closing brace of a ruleset in the same column as the first
  character of the ruleset.
* Separate each ruleset by a blank line.

```css
.selector-1,
.selector-2,
.selector-3[type='text'] {
  background: #fff;
  background: linear-gradient(#fff, rgba(0, 0, 0, 0.8));
  box-sizing: border-box;
  color: #333;
  display: block;
  font-family: helvetica, arial, sans-serif;
}

.selector-a,
.selector-b {
  padding: 10px;
}
```

#### Declaration order

Declarations are to be ordered alphabetically.

```css
.selector {
  background: #000;
  border: 10px solid #333;
  bottom: 0;
  box-sizing: border-box;
  color: #fff;
  display: inline-block;
  font-family: sans-serif;
  font-size: 16px;
  height: 100px;
  left: 0;
  margin: 10px;
  overflow: hidden;
  padding: 10px;
  position: absolute;
  right: 0;
  text-align: right;
  top: 0;
  width: 100px;
  z-index: 10;
}
```

#### Exceptions and slight deviations

Large blocks of single declarations can use a slightly different, single-line
format. In this case, a space should be included after the opening brace and
before the closing brace.

```css
.selector-1 { width: 10%; }
.selector-2 { width: 20%; }
.selector-3 { width: 30%; }
```

Long, comma-separated property values - such as collections of gradients or
shadows - can be arranged across multiple lines in an effort to improve
readability and produce more useful diffs. There are various formats that could
be used; one example is shown below.

```css
.selector {
  background-image:
    linear-gradient(#fff, #ccc),
    linear-gradient(#f3c, #4ec);
  box-shadow:
    1px 1px 1px #000,
    2px 2px 1px 1px #ccc inset;
}
```

### Preprocessors: additional format considerations

We use Sass as our preprocessor with the following rules:

* Limit nesting to 1 level deep. Reassess any nesting more than 2 levels deep.
  This prevents overly-specific CSS selectors.
* Avoid large numbers of nested rules. Break them up when readability starts to
  be affected. Preference to avoid nesting that spreads over more than 20
  lines.
* Always place `@extend` statements on the first lines of a declaration
  block.
* Where possible, group `@include` statements at the top of a declaration
  block, after any `@extend` statements.
* Consider prefixing custom functions with `x-` or another namespace. This
  helps to avoid any potential to confuse your function with a native CSS
  function, or to clash with functions from libraries.

```scss
.selector-1 {
  @extend .other-rule;
  @include clearfix();
  width: x-grid-unit(1);
  // other declarations
}
```
<a name="vendor-prefixes"></a>
## 5. Vendor Prefixes

Please do not use vendor prefixes or Sass mixins to provide prefixes.

Write all CSS properties using web standards and run Autoprefixer over your CSS to provide vendor prefixes. An example can be found in the [project boilerplate](https://github.com/finderau/project-boilerplate).

<a name="naming-convensions"></a>
## 6. Naming Convensions

Our CSS naming convensions are designed to make your code more transparent and more informative.

A good name for a class should consider:

1. What type of thing a class does.
2. Where a class can be used.
3. What (else) a class might be related to.
4. Written in English.

The naming convention we follow is very simple: hyphen (-) delimited strings, with [BEM-like](http://cssguidelin.es/#bem-like-naming) naming for more complex pieces of code.

### Example 

```
.room {} /* Root element for a component */
.room__door {} /* An element within the component */
.room--kitchen {} /* A modifier of the original component */
```

<a name="validating-css"></a>
## 7. Validating Scss

All Scss code should be validated using Scss Lint. An example can be found in the [project boilerplate](https://github.com/finderau/project-boilerplate).

<a name="example"></a>
## 8. Practical example

An example of various conventions.

```css
/* ==========================================================================
   Grid layout
   ========================================================================== */

/**
 * Column layout with horizontal scroll.
 *
 * This creates a single row of full-height, non-wrapping columns that can
 * be browsed horizontally within their parent.
 *
 * Example HTML:
 *
 * <div class="grid">
 *     <div class="cell cell-3"></div>
 *     <div class="cell cell-3"></div>
 *     <div class="cell cell-3"></div>
 * </div>
 */

/**
 * Grid container
 *
 * Must only contain `.cell` children.
 *
 * 1. Remove inter-cell whitespace
 * 2. Prevent inline-block cells wrapping
 */

.grid {
    height: 100%;
    font-size: 0; 
    white-space: nowrap;
}

/**
 * Grid cells
 *
 * No explicit width by default. Extend with `.cell-n` classes.
 *
 * 1. Set the inter-cell spacing
 * 2. Reset white-space inherited from `.grid`
 * 3. Reset font-size inherited from `.grid`
 */

.cell {
  border: 2px solid #333;
  box-sizing: border-box;
  display: inline-block;
  height: 100%;
  font-size: 16px;
  overflow: hidden;
  padding: 0 10px;
  position: relative;
  vertical-align: top;
  white-space: normal;
}

/* Cell states */

.cell.is-animating {
  background-color: #fffdec;
}

/* Cell dimensions
   ========================================================================== */

.cell-1 { width: 10%; }
.cell-2 { width: 20%; }
.cell-3 { width: 30%; }
.cell-4 { width: 40%; }
.cell-5 { width: 50%; }

/* Cell modifiers
   ========================================================================== */

.cell--detail,
.cell--important {
    border-width: 4px;
}
```

<a name="acknowledgements"></a>
## Acknowledgements

Based on a work at
[github.com/necolas/idiomatic-css](https://github.com/necolas/idiomatic-css).
[cssguidelin.es/#bem-like-naming](http://cssguidelin.es/#bem-like-naming)
