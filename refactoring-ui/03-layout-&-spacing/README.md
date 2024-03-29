# 03. Layout & Spacing

## Start with whitespace

- initial designs should have a lot of whitespace
- as you start to clean it up, you should REMOVE it, not ADD it
- it is much easier to remove than add it to achieve good designs
- only time you should start with little whitespace is with dashboards were a lot of info is compacted

## Spacing & sizing system

- create one before you start designing
- tailwind already comes with one so another reason to use it :)

## Don't fill the whole screen

- limit the max-width to your UI to 1200-1400px for desktops
- for forms, cards, etc, limit them to 600px
- start designing for mobile first (~400px vw) and expand and change it to tablet and then desktop
- some sizing will stay the same from mobile to desktop

## Grids are overrated

- grids are good but don't rely on them for your entire layout
- tradtionally, for dashboards, the aside nav menu on the left would take up 3 columns out of 12 (25% width) while the main content takes 9
- this gets akward as the viewport changes
- instead give the nav menu a fixed width and then use flex for the dashboard so that, when the viewport changes, only the elements in the main section change accordingly
- TLDR, use fixed widths more often especially for components you don't want changing as the viewport changes

## Relative sizing doesn't scale

- having a catch-all doesn't work all the time, e.g. `2.5em` for headings
- it may look fine on desktop but TOO BIG on mobile
- therefore, sometimes you will use hard coded values, e.g. `2.5em` for headings on desktop and `24px` on mobile
- As a general rule, elements that are large on large screens need to shrink
  faster than elements that are already fairly small — the difference between
  small elements and large elements should be less extreme at small screen
  sizes.

## Ambigious sizing

- has to do with law of attraction
- elements that are in a group should be spaced closer together and spaced farther away from other groups
