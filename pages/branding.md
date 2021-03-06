# Branding Guidelines

## Table of contents
1. [General principles](#general-principles)
2. [Colours](#colours)
3. [Typefaces](#font-type)
4. [Size of text](#font-sizes)
5. [Weight of text](#font-weights)
6. [Logo](#logo)
7. [Forms](#forms)
8. [Graphs](#graphs)
9. [Examples](#examples)

<a name="general-principles"></a>
## 1. General principles
* We use [flat design](http://www.hongkiat.com/blog/flat-design-resources/) elements as part of our design aesthetics
* Do not use gradients

<a name="colours"></a>
## 2. Colours

We have two brand colours. These should be used sparingly and not be used in very large blocks of colours.

### Brand Colours

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](./images/1591fe.png) | Primary | #1591fe |Icons, highlight
![](./images/18304b.png) | Secondary | #18304b | Main headings, navigation, icons

### Grey tones
For consistency, we try to use these greyscale values throughout our interfaces.

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](./images/010101.png) | Body | #010101 | Body content
![](./images/777.png) | Disclaimers | #777 | Disclaimers
![](./images/e5e5e5.png) | Box 1 | #e5e5e5 | Boxes
![](./images/f5f5f5.png) | Box 2 | #f5f5f5 | Boxes

### Call to Action

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](./images/27ae60.png) | Green | #27ae60 | Primary call to action buttons
![](./images/f17935.png) | Orange | #f17935 | Text links, hover state and  more info buttons


### Blue tones

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](./images/e6f3ff.png) | Light blue | e6f3ff | Backgrounds when more prominence is needed vs a grey background
![](./images/d0e9ff.png) | Mid blue | #d0e9ff | Dividing lines on light blue background, forms and tooltips 
![](./images/0076cc.png) | Dark blue | #0076cc | Links and comparison tables

### System
These are not part of our brand, but we use these in special cases.

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](./images/dd4b39.png) | Red | #dd4b39 | Error messages
![](./images/fc0.png) | Yellow | #fc0 | Warning messages
![](./images/d14.png) | Crimson | #d14 | Giving emphasis

<a name="font-type"></a>
## 3. Typefaces

We use [Proxima Nova](http://www.marksimonson.com/fonts/view/proxima-nova) for all of our text and headings.

![](./images/proxima.png)

### Alternative to Proxima Nova
```css
body {
    font-family: proxima-nova, Helvetica, Arial, sans-serif;
}
```

<a name="font-sizes"></a>
## 4. Text size

Element | Size
--- | ---
base | 15px
h1 | 2em
h2 | 1.8em
h3 | 1.6em
h4 | 1.4em
h5 | 1.2em
h6 | 1em

<a name="font-weights"></a>
## 5. Text weight

Weight | Value
--- | ---
normal | 400
semibold | 600
bold | 600

<a name="logo"></a>
## 6. Logo

The company logo is an important and valued graphic element and must be used
consistently and appropriately, even minor variations will undermine and compromise
the image of the branding.

![](./images/logo-good.png) ![](./images/logo-bad.png)

<a name="forms"></a>
## 7. Forms

### Labels
![](./images/labels.png)

``` css
label {
  display: block
  font-size: .867em; /* 13px */
  font-weight: 600;
}
```

### Text Inputs
![](./images/text-inputs.png)

``` css
input[type="text"] {
  background: #fff;
  border: 1px solid #d8d8d8;
  border-radius: 4px;
  box-shadow: 1px 1px 3px #e5e5e5 inset;
  color: #777;
  padding: .5em;
}
```

### Fieldsets

Used to group form elements

![](./images/fieldsets.png)

``` css
fieldset {
  border: 0;
}
 
/* If form has more than one fieldset, add class to show a mid-blue bottom border */
fieldset.form_divider {
  border-bottom: 1px solid #d0e9ff;
  margin-bottom: 10px;
  padding-bottom: 10px;
}
```

### Dropdowns

![](./images/dropdowns.png)

``` css
select {
  background: #fff;
  border: 1px solid #d8d8d8;
  border-radius: 4px;
  box-shadow: 1px 1px 3px #e5e5e5 inset;
  color: #777;
  padding: .5em;
}
```

### Errors

![](./images/errors.png)

```
.error {
    color: #dd4b39;
    display: block;
    font-size: .867em;
}
 
.error-input {
    border: 1px solid #dd4b39;
}
```

### Sliders

![](./images/sliders.png)

``` css
.slider {
  background-color: #e5e5e5; /* Fallback */
  background-image: linear-gradient(top, #e5e5e5, #eee);
  background-repeat: repeat-x;
  border-radius: 4px;
  box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
  height: 10px;
}
 
.slider__handle {
  background-color: #1591fe;
  background-repeat: repeat-x;
  border-radius: 20px;
  box-shadow: inset 0 1px 0 rgba(255,255,255,.2),0 1px 2px rgba(0,0,0,.05);
  height: 20px;
  width: 20px;
}
```

### Buttons

![](./images/buttons-good.png) ![](./images/buttons-bad.png)

```css
.btn {
  border-radius: 4px;
  box-shadow: 0 2px 2px rgba(0,0,0.15);
  color: #fff;
  font-weight: 600;
  text-align: center;
}
```

#### Sizes

![](./images/btn-xsml.png)
![](./images/btn-sml.png)
![](./images/btn-default.png)
![](./images/btn-lrg.png)

``` css
.btn {
  font-size: 1em; /* 15px */
  padding: .75em 1em;
}

.btn--xsml {
  font-size: .733em; /* 11px */
  padding: 1em 2.3em;
}

.btn--sml {
  font-size: .867em; /* 13px */
  padding: .4em 1.8em;
}

.btn--lrg {
  font-size: 1.2em /* 18 */
  padding: 1em 2.3em;
}
```

<a name="graphs"></a>
## 8. Graphs

Do not use gradients. Use flat colours for graphs and charts.

![](./images/graph-good.png) ![](./images/graph-bad.png)
![](./images/graph-2-good.png) ![](./images/graph-2-bad.png)

<a name="examples"></a>
## 9. Examples

### Borders
![](./images/borders-good.png) ![](./images/borders-bad.png)

```css
selector {
  border: 1px solid #d8d8d8;
}
```

### Iconography

Where possible icons should use a vector format, either an icon font or SVG with PNG fallback for IE8.
![](./images/icons-good.png) ![](./images/icons-bad.png)

### Tabs
![](./images/tabs-good.png) ![](./images/tabs-bad.png)

#### Active tab
```css
.tab--active {
  background-color: #fff;
  color: #0076cc;
  font-size: 14px;
  font-weight: 600;
  padding: 8px 15px;
  text-align: center;
}
```

#### Inactive tab
```css
.tab--inactive {
  background-color: #e5e5e5;
   color: #18304b;
}
```

### Tables

![](./images/table-good.png) ![](./images/table-bad.png)

### Tooltips

![](./images/tooltip.png)

``` css
.tooltip {
  background-color: #d0e9ff; /* mid-blue */
  border-radius: 4px;
  box-shadow: 0 2px 2px rgba(0,0,0,.25);
  color: #010101;
  font-size: 11px;
  padding: 10px 5px;
}
 
/* Tooltip down arrow using css triangles */
.tooltip::after {
  border-bottom-color: #d0e9ff; /* mid-blue */
  border-width: 0 10px 10px;
}
```
