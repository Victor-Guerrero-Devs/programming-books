# 02. Hierarchy is Everything

## Not all elements are equal

- visual hierarchy is the most important thing when it comes to producing great designs
- the purpose is to make the important things pop out with size and color and downplaying the secondary and tertiary details by decreasing size and muting the color

## Size isn’t everything

- using font-size alone to establish hierarchy is not smart
- instead, you should incorporate color and font-weight as well
- this way you don't have have extremly huge headings and small body text
- you headings can be medium sized with a thicker weight and brighter color to pop out instead of relying on font-size alone
- stick to 2 or 3 colors at most, e.g. dark gray for headings, medium gray for regular text, light gray for copyright
- 600-700 font-weight for headings, 400-500 for regular text
- never dip below 400; use a lighter color or smaller font-size instead

## Don’t use grey text on colored backgrounds

- use it only if you have a white background
- if you are trying to de-emphasize text, give it a lighter color/opacity of the background it has, e.g. if a blue background, give it a very light blue font color

## Emphasize by de-emphasizing

- sometimes you will not be able to emphasize the primary element anymore
- to solve this, just de-emphasize the other elements
- primarily achieved by giving the less important elements a color that helps them blend in, e.g. your main background is a light blue and both your main section and aside section use a white bg to help them pop out. To fix the competition, give the aside section the same light blue background

## Labels are a last resort

- labels should only be reserved for forms
- say you have a card component for users that display their name, job title, email, and phone number
- you don't have to add before each one a label to specify what the value is supposed to be
- it is self-evident
- sometimes labels are needed outside of forms like a product item card
- in this case, you need to blend the label into the value, e.g. not `stock: 12` but `12 in stock`
- sometimes labels are absolutely needed when presenting data like a fitness report
- in this case, make them bold because more than likely a user will be looking for a specific piece of data

## Separate visual hierarchy from document hierarchy

- sometimes, the main header of a page should be large to tell the user what the content it contains will be about
- nevertheless, in this case they usually act as labels
- thus, these kinds of heading should be down played so as not to steal attention from the main content

## Balance weight and contrast

- bolded elements pop out more simply by the virtue of taking up more space than other elements
- when putting solid icons next to text, they draw attention to the text itself
- this can through off your visual hierarchy since most of the time
- to correct this issue, lower the opacity of the icons and the text next to it

## Semantics are secondary

- say you have a card with 3 buttons for three different actions
- the most important one should pop out the most via color
- the secondary one should have a neutral bg color
- the tertiary one should have a bg color that matches the background to downplay it the most
- finally, for destructive actions like deleting something, use red bg color
