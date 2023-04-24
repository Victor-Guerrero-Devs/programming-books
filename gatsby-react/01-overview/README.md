# 01. Overview of Gatsby

## History of Static Web

Static sites are the original blueprint for any website using HTML, CSS, and JS.
CMSes were created to allow non-technical users to control a webpage's design and content, but they can be clunky and slow.
Frontend frameworks and libraries, such as React.js, have gained notoriety and have drastically sped up workflows.
However, combining frontend frameworks with CMSs can lead to security and bottleneck issues, leading to the rebirth of static sites.
Gatsby was created by Kyle Mathews, who identified gaps in existing tooling and wanted to create an ideal product for website accessibility and performance.
Static content is unbeatable in terms of speed and performance.

## What is Gatsby

Gatsby is a static site generator that uses React.
Static site generators create static pages from a template or component and supplement them with content from a source.
They're an alternative to traditional database-driven CMS like WordPress.
Static site generators like Gatsby generate pages during a build process, eliminating the latency that databases would introduce.
Gatsby pages are composed of HTML, JS, and CSS files, and can be served via a CDN pointing to a storage medium (like AWS S3 bucket)
Gatsby offers server-side and deferred static generation, rendering functionality for when static generation is not enough.
Gatsby offers a focus on developer experience, and its ease of use can be broken down into four steps.

## Source Content from Anywhere

Gatsby allows for sourcing data from various sources and combining them into a unified data layer
Gatsby community provides source plugins to easily ingest data from different sources without the need for code
The data can be explored and queried using a uniform data layer powered by GraphQL
GraphQL layer is transitory and doesn't affect the size of the production site
The process of sourcing and querying data is explained in Chapter 3 of the book.
