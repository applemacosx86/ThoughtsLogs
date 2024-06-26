---
title : 'Setup Search Page'
date : 2024-06-26T22:51:04+08:00
draft : false
cover: 
    image: imgs/hugosearch-Screenshot 2024-06-26 at 22.59.25.jpg
    alt: 'This is the cover image'
    caption: 'screenshot'
tags: ["hugo"]
categories: ["tech"]
---

# How to Setup the Hugo Search Page

[Solution from Github](https://github.com/adityatelange/hugo-PaperMod/wiki/Features#search-page)

### Search Page
PaperMod uses Fuse.js Basic for search functionality
Add the following to site config, config.yml

    outputs:
    home:
        - HTML
        - RSS
        - JSON # necessary for search

Create a page with search.md in content directory with following content

    ---
    title: "Search" # in any language you want
    layout: "search" # necessary for search
    # url: "/archive"
    # description: "Description for Search"
    summary: "search"
    placeholder: "placeholder text in search input box"
    ---
To hide a particular page from being searched, add it in post's frontmatter

    searchHidden: true