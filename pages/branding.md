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
![](../images/1591fe.png) | Primary | #1591fe |Icons, highlight
![](../images/18304b.png) | Secondary | #18304b | Main headings, navigation, icons

### Grey tones
For consistency, we try to use these greyscale values throughout our interfaces.

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](../images/010101.png) | Body | #010101 | Body content
![](../images/777.png) | Disclaimers | #777 | Disclaimers
![](../images/e5e5e5.png) | Box 1 | #e5e5e5 | Boxes
![](../images/f5f5f5.png) | Box 2 | #f5f5f5 | Boxes

### Call to Action

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](../images/27ae60.png) | Green | #27ae60 | Primary call to action buttons
![](../images/f17935.png) | Orange | #f17935 | Text links, hover state and  more info buttons


### Blue tones

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](../images/e6f3ff.png) | Light blue | e6f3ff | Backgrounds when more prominence is needed vs a grey background
![](../images/d0e9ff.png) | Mid blue | #d0e9ff | Dividing lines on light blue background, froms and tooltips 
![](../images/0076cc.png) | Dark blue | #0076cc | Links and comparison tables

### System
These are not part of our brand, but we use these in special cases.

Colour | Name | Hex | Used in
--- | --- | --- | ---
![](../images/dd4b39.png) | Red | #dd4b39 | Error messages
![](../images/fc0.png) | Yellow | #fc0 | Warning messages
![](../images/d14.png) | Crimson | #d14 | Giving emphasis

<a name="font-type"></a>
## 3. Typefaces

We use [Proxima Nova](http://www.marksimonson.com/fonts/view/proxima-nova) for all of our text and headings.

![](../images/proxima.png)

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

TBC

<a name="forms"></a>
## 7. Forms

TBC

<a name="graphs"></a>
## 8. Graphs

TBC

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
![](./images/icons-good.png) ![](./images/icons-bad.png)

### Tabs
Good | Off-brand
--- | ---
![](../images/tabs-good.png) | ![](../images/tabs-off.png)

#### Active tab
```css
.active-tab {
  background-color: #fff;
  color: #18304b;
  font-size: 14px;
  font-weight: 600;
  padding: 8px 15px;
  text-align: center;
}
```

#### Inactive tab
```css
.inactive-tab {
  background-color: #e5e5e5;
}
```

### Tables

Good | Off-brand
--- | ---
![](../images/table-good.png) | ![](../images/table-off.png)
