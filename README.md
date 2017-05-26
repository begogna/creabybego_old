# Personal website for Bego

## Getting started

git clone [this repository]

Install dependencies
```
bundle install
```

Start development server
```
bundle exec jekyll serve --watch
```

## Directory structure

Below is the most important folder hierarchy that the Jekyll template uses

```
.
├── assets
│   ├── css
│   ├── fonts
│   ├── js
│   └── sass - sass goes here (main.scss contains most of the styles)
├── images
│   ├── fulls - Full size images
│   └── thumbs - Thumbnails
├── _includes
├── _items - All items, one markdown file per item.
├── _layouts - Different Jekyll layouts.
├── _sections - All categories, one markdown file per category.
└── _site - The generated site.
```

## Add new item

Create new markdown file in _items, the name of the file will become
its url so choose appropriate file names use "-" as delimiter.

Example _items/my-new-item.md will be available under .../items/my-new-item/

```
---
layout: item
title: 'Example title'
category: 'Example category' 
excerpt: 'Little example summary'
---

Then the content goes here... in markdown or html...
```

## Add new section

Create a new markdown file in _sections.

A section has the following properties:

```
---
layout: section
name: 'Example name'
excerpt: 'Little example summary.'
image: '/images/thumbs/example.jpg'
---
```
No other content is needed for a section.
