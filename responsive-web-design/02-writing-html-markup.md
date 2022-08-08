# 02. Writing HTML Markup

## Intro

Many believe that writing HTML is simple yet many do not know the correct way to write HTML. As a consequence, the general skeleton of their webpage is malformed.

This chapter, therefore, will be dedicated to writing HTML well.

## Semantic Elements

Before semantic elements, every container used a div. In order to find out what that div contained was to look at its class name.

Nowadays, we have new elements that act like divs except they give some indication of what they contain.

### main

This is used to contain the main content of a webpage, the content that is unique to that webpage.

There should only be one of these per HTML file and it should only be nested inside of the body element, i.e. it shoudn't be nested inside an `article, aside, header, footer` etc, but it is fine for these to be nested inside of main

### section

- used to define a generic section of a document or application
- for containing small elements, continue to use divs as their container
- sections are for grouping together related things like the about section, contact section, plans section, testimonial section etc

### nav

- used to wrap major navigational links to other pages or parts within the same page.
- reserved for the main nav bar at the top of a page

### article

- these are usually confused with `<section></section>`
- biggest difference is that `section` encapsulates a larger amount of content whereas the `article` encapsulates a smaller amount
- ex: `section` is used for containing all the different plans a customer can use but `article` is used to contain the individual plan cards
- therefore, `article` is nested inside of `section` and never the other way

### aside

- used for content that is tangentially related to the content around it.
- use it for sidebars, or content as a little tip about a related subject in a blog post or "You may also like..." or "Customers who bought this also bought..."
- basically, anything not directly related to the main content would work well

### header

- can be used in many ways
- as the container for your nav bar
- nested inside every `section` and `article` as a container for `hx` elements

### footer

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

## Don't use h1-h6 as markup

Don't use them for stylistic reasons; only use them for giving a heading to a new section or sub-section

```html
<h1>Welcome to my blog</h1>
<h2>where anything and everything is discussed</h2>
```

That is a badway to use h2 because it is being used as a subtitle when it should be used strictly as a heading to a new section

```html
<h1>Welcome to my blog</h1>
<p>where anything and everything is discussed</p>

<h2>Blog Post #1</h2>
```

This is how it should be done. Give the p element a class and style instead of using an h2

## p + blockquote

the `blockquote` is usually preceeded by a `p` as a form of introduction

```html
<p>Hemingway once wrote that:</p>
<blockquote>
  The world breaks everyone and afterward many are strong at the broken places
</blockquote>
```

## figure + figcaption

Figure is used as a container for both `img` and `figcaption`

Although `figcaption` provides some text for the `img`, the alt attribute should still contain something for assistive tech

```html
<figure>
  <img src="imgs/dog.jpg" alt="a dog drinking water" />
  <figcaption>
    Here is a picture of my dog when he was just two years old
  </figcaption>
</figure>
```

## details + summary

```html
<details>
  <summary>I ate 15 scones in one day</summary>
  <p>
    Of course I didn't. It would probably kill me if I did. What a way to go.
    Mmmmmm, scones!
  </p>
</details>
```

This is a budget accordion. To left of the content in `summary`, there will be an arrow icon that can be clicked (actually both the icon and summary text are clickable).

Once it is clicked, it will show the content in `p`
