# Browser Support

## Table of contents
1. [Browsers](#browsers)
2. [Responsive Web Design](#responsive)
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
## Responsive Web Design

Building a responsive or mobile-friendly project is a massive topic on its own, and because a lot of good resources are already online, we’ll just provide some pointers.

All content on finder.com.au must be responsive, capable of supporting any screen resolution.

Begin with a mobile-first philosophy. Resize your browser window to a “mobile” size. To help with this, Firefox introduced a pretty cool Responsive Design View mode in version 15. Or you can use the Web Developer Toolbar extension, available for both Firefox and Chrome.

As a minimum requirement content must be able to render at the following widths:

Width | Common usage
--- | --- 
up to 640px | mobile 
750px | content next to a side bar (narrow desktop)
895px | content next to a side bar (large desktop)
972px | full width narrow desktop
1120px | full width large desktop

When you’re happy with the basic styling on desktop browsers, start testing some real devices. Things will need adjusting, and issues will arise that don’t appear on the desktop.
Things to watch out for:

* Click/touch events
* Animation performance
* Retina images

<a name="cross-browser"></a>
## Cross browser compatibilty

All content doesn't have to look the same across every browser. Our general rules in this area are:

1. Mobile first where ever possible
2. Progressively enhance features
3. Ensure graceful degredation on unsupported features
4. All modern browsers should look consistent

Older browsers like IE8 are supported, but they only need to be functional. For example, if we use `border-radius` we don't mind when IE8 doesn't understand this property and renders the corners as square.

