# 02. Writing HTML Markup

## Intro

Many believe that writing HTML is simple yet many do not know the correct way to write HTML. As a consequence, the general skeleton of their webpage is malformed.

This chapter, therefore, will be dedicated to writing HTML well.

## Semantic Elements

Before semantic elements, every container used a div. In order to find out what that div contained was to look at its class name.

Nowadays, we have new elements that act like divs except they give some indication of what they contain.

### <main>

This is used to contain the main content of a webpage, the content that is unique to that webpage.

There should only be one of these per HTML file and it should only be nested inside of the body element, i.e. it shoudn't be nested inside an `article, aside, header, footer` etc, but it is fine for these to be nested inside of main

### <section>

- used to define a generic section of a document or application
- for containing small elements, continue to use divs as their container
- sections are for grouping together related things like the about section, contact section, plans section, testimonial section etc

### <nav>

- used to wrap major navigational links to other pages or parts within the same page.
- reserved for the main nav bar at the top of a page

### <article>

- these are usually confused with `<section></section>`
- biggest difference is that `section` encapsulates a larger amount of content whereas the `article` encapsulates a smaller amount
- ex: `section` is used for containing all the different plans a customer can use but `article` is used to contain the individual plan cards
- therefore, `article` is nested inside of `section` and never the other way

### <aside>

- used for content that is tangentially related to the content around it.
- use it for sidebars, or content as a little tip about a related subject in a blog post or "You may also like..." or "Customers who bought this also bought..."
- basically, anything not directly related to the main content would work well

### <header>

- can be used in many ways
- as the container for your nav bar
- nested inside every `section` and `article` as a container for `hx` elements

### <footer>

- works the same way as `header`
- can be used for the last section on a webpage
- can also be nested inside of a blog post `article` containg info about the writer etc

## HTML5 outline algorithm

- usually, webpages should only have one `h1`
- w/ HTML5, each individual section can have its own `h1`
- however, most search engines don't follow the HTML5 outline regulations so stick to one `h1` per page so they can know the main content

Check your pages' outline here

• http://gsnedders.html5.org/outliner/
• http://hoyois.github.com/html5outliner/
