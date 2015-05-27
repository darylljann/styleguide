# JavaScript Guidelines

The following document outlines a how developers at finder.com.au write JavaScript to ensure all work is reliable and consistent.

We are inspired by projects like [Idiomatic JS](https://github.com/rwaldron/idiomatic.js/) and [JSLint](http://jslint.com/).

This is a living document and new ideas are always welcome. Please contribute.

## Table of contents

1. [General principles](#general-principles)
2. [Supported Libraries](#supported-libraries)
3. [Validation](#validation)
4. [Naming Conventions](#naming-conventions)
5. [Testing](#testing)

<a name="general-principles"></a>
## 1. General principles

* JavaScript must be validated using JSHint
* Avoid using globals where ever possible
* Use Bower to import third party dependancies (eg. jquery, charts etc.) or store them inside a `/vendor` folder
* If you have multiple JavaScript files, you must combine and minify them into one to improve performance and reduce additional http requests.
* All code names, descriptions and comments must be in English.

## 2. Supported libraries

Name | Version
--- | --- 
Barebones Share Buttons | 0.2.0
Enquire | 2.1.2
Handlebars | 1.3.0
jQuery | 1.7.2
jQuery Validation | 1.10.0

## 3. Validating JavaScript

All JavaScript written for finder.com.au must pass strict JSHint rules. These rules can be found in the [project boilerplate]().

## 4. Naming conventions

Ensure that your code is written in a way that is friendly to humans. All JavaScript will be uglified, which will optimise most variables to conserve bandwidth.

1. use camelCase
2. write all names in English

### Bad example
```javascript
function q(s) {
  return document.querySelectorAll(s);
}
var i,a=[],els=q("#foo");
for(i=0;i<els.length;i++){a.push(els[i]);}
```

### Good example

```javascript
function query( selector ) {
  return document.querySelectorAll( selector );
}

var idx,
  elements = [],
  matches = query("#foo"),
  length = matches.length;

for (idx = 0; idx < length; idx++ ) {
  elements.push( matches[ idx ] );
}
```

## 5. Testing

Unit tests should use Jasmine. An example can be found in the [project boilerplate](https://github.com/finderau/project-boilerplate)
