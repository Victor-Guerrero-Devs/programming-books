# 01. Starting from Scratch

## Start with a feature, not a layout

You should begin designing, not with the overall layout, but with a specific component. Say you are building a UI for an Airline for booking flights. Therefore, you should start with a specific component like the search bar for flights.

• A field for the departure city
• A field for the destination city
• A field for the departure date
• A field for the return date
• A button to perform the search

This way you avoid over-designing or adding unneeded styles.

## Detail comes later

- don't get bogged down with low-level design decisions like typefaces and colors in the early stages of designing a new feature
- the focus should be on exploring layout ideas and creating a clear interface with a strong hierarchy
- you should beging with paper and pen instead
- low-fidelity designs like sketches and wireframes are disposable and should be used to explore ideas before moving on to building the real thing
- just use different shades of gray to begin with

## Don’t design too much

- once you have a basic model of how a feature should look like, start building it
- don't sit around and think about all the edge cases; these can be solved after the intial implementation
- build the real thing as early as possible and reiterate over it (i.e. design then code, repeat)
- say you want to build a comment section that allows users to upload stuff so a button will be needed + the functionality
- you find out that adding this functionality will take a lot more than expected; nevertheless, implement the design and worry about it later

## Choose a personality

- a banking app will want to look serious; a new start-up playful and fun
- these
- these personalities are communicated via font and colors and border radius
- serious = serif, gray, blue, gold, square ; playful = rounded sans serif, pink, rounded buttons ; neutral = sans serif

## Limit your choices

- this relates to your colors, fonts, font-sizes, and sizes in general
- since tailwind already has a built in system for all of these (except fonts), it will be easy when using it
- when choosing colors on your own, just pick 3 and then make an ~8 shade variation of each
- for any subsequent projects, incoporate those colors gradients
