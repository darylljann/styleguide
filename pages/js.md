# JavaScript

1. [Supported Libraries](#supported-libraries)
2. [Validation](#validation)
3. [Naming Conventions](#naming-conventions)
4. [Testing](#testing)

## 1. Supported libraries

Name | Version
--- | --- 
Handlebars | 1.3.0
Enquire | 2.1.2
jQuery | 1.7.2
jQuery Validation | 1.10.0
Barebones Share Buttons | 0.2.0

## 2. Validating JavaScript

All JavaScript written for finder.com.au must pass strict JSHint rules. These rules can be found in the [project boilerplate]().

## 3. Naming conventions

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

var idx = 0,
  elements = [],
  matches = query("#foo"),
  length = matches.length;

for ( ; idx < length; idx++ ) {
  elements.push( matches[ idx ] );
}
```

## 4. Testing

Unit tests should use Jasmine. An example can be found in the [project boilerplate](https://github.com/finderau/project-boilerplate)
