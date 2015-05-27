# Browser Support

## Table of contents
1. [Browsers](#browsers)
2. [Responsive](#responsive)
3. [Cross browser compatibilty](#cross-browser)


<a name="browsers"></a>
## Browsers

Name | Min Version
--- | --- 
Chrome | Two versions previous
FireFox | Two versions previous
Internet Explorer | IE8+
Safari Desktop | 8+
iOS | iOS7+
Android | 4.1+
Android Chrome | Two versions previous


<a name="responsive"></a>
## Responsive

All content on finder.com.au must be responsive, capable of supporting any screen resolution.

As a minimum requirement content must be able to render at the following widths:

Width | Common usage
--- | --- 
up to 640px | mobile 
750px | content next to a side bar (narrow desktop)
895px | content next to a side bar (large desktop)
972px | full width narrow desktop
1120px | full width large desktop

<a name="cross-browser"></a>
## Cross browser compatibilty

All content doesn't have to look the same across every browser. Our general rules in this area are:

1. Mobile first where ever possible
2. Progressively enhance features
3. Ensure graceful degredation on unsupported features
4. All modern browsers should look consistent

Older browsers like IE8 are supported, but they only need to be functional. For example, if we use `border-radius` we don't mind when IE8 doesn't understand this property and renders the corners as square.

