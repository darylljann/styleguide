# Important information for third party developers

## Table of contents

1. [Scoping CSS](#scoping-css)
2. [JavaScript libraries](#javascript-libraries)

<a name="scoping-css"></a>
## 1. Scoping CSS

To ensure that your CSS doesn't clash with CSS on finder.com.au we recommend that you prefix your selectors with `tui-` which stands for 'third party user interface'.

### Bad 

This is bad as it is the same classname used by finder.com.au buttons and links.
```
.btn {
  
}
```

### Good
We now know this is a third party implementation of a button.
```
.tui-btn {
	
}
```
<a name="javascript-libraries"></a>
## 2. JavaScript Libaries

Make sure you're understood what JavaScript libraries we support on finder.com.au. If you need to use something else please let your contact at finder know what you need and we will assist with supporting that library if we can. This is especially important if you're working on a project that requires a MVC framework.
