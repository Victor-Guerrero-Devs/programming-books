# 03. Media Queries

## viewport meta tag

When Apple released the iPhone in 2007, they introduced a new `meta` tag for the viewport to allow webpages to adjust themselves for mobile browsers.

`<meta name="viewport" content="initial-scale=1.0, user-scalable=no" />`

As long as you have that line in your `head` element, responsive design will be a breeze because it takes the physical pixels of the device into account.

## Why media queries are needed for a responsive web design

There are a ton of different properties we can check for w/ media queries but the thing we want to check for is **width**

Once the viewport hits a certain width, we can activate/change CSS styles to accomdate the new viewport
