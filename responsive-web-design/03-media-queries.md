# 03. Media Queries

## viewport meta tag

When Apple released the iPhone in 2007, they introduced a new `meta` tag for the viewport to allow webpages to adjust themselves for mobile browsers.

`<meta name="viewport" content="initial-scale=1.0, user-scalable=no" />`

As long as you have that line in your `head` element, responsive design will be a breeze because it takes the physical pixels of the device into account.

## Why media queries are needed for a responsive web design

There are a ton of different properties we can check for w/ media queries but the thing we want to check for is **width**

Once the viewport hits a certain width, we can activate/change CSS styles to accomdate the new viewport

## Conditional Logic

Media queries use conditional logic

```css
@media screen and (min-width: 320px) {
  body {
    background-color: green;
  }
}
```

In other words, if the viewport width is at least 320 pixels, change the background color of the body element to green.

## Separating media queries

Instead of throwing together all of you CSS changes into one media query, it is advised to use multiple media queries for each component.

Example: just like you should split your CSS file into different sections via headings (or split them into different files), you should use multiple media queries for that particular section

Therefore, the `header` should have it own media query, the `about-section` should have its own too, and the `footer`
