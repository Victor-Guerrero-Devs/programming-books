# 04. Fluid Layout -- Flexbox and Responsive Images

## Intro

- the three core tenets of responsive web design were introduced: fluid layout, media queries, and flexible media. 
- In this chapter, the focus is on fluid layout and flexible media. 
- The chapter explains that fluid layouts, which were popular in the past, offer benefits that fixed-width designs don't. The chapter then explains how to use CSS Flexbox to create fluid layouts and outlines its benefits. 
- The chapter also covers how to convert fixed pixel layouts to proportional sizes and how to use responsive images and srcset for resolution switching and art direction. 
- The chapter concludes with a reminder that converting fixed designs into fluid relationships is a task that needs to be performed constantly when building responsive web designs.

## From Fixed Pixels to Responsive Units

- just use a max-width to set a limit to the container above 1020px vw 
- use percentage units for anything smaller

## Flexbox?

- the fix to floats and tables
- easy to position items on the x and y axis
- easy to create layouts 
- easy to be responsive

## Stickied Footer

- always a pain to make the footer stick the bottom especially when there isn't content to push it there 
- easy to do with flex

```html
<body>
    <main>blah</main>
    <footer>blagh</footer>
</body>
```

```css
body {
    display: flex;
    min-height: 100%;
}

main {
    flex: 1 0 auto;
}
```

That one flex in `main` says stretch out as vertically as you can which will make the footer take up and stay only at the bottom.