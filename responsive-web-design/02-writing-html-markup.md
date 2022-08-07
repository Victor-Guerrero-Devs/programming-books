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
