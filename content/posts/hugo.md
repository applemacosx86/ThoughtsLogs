---
title : 'Hugo Learning Memo'
date : 2024-06-20T22:53:04+08:00
draft : false
tags: ["hugo"]
categories: ["tech", "memo"]
---

## frontmatter关于tags/categories可以这样写
tags: [zsh]
categories: [tech,shell]

## How to insert an image

![How to insert an image](https://stackoverflow.com/questions/71501256/how-to-insert-an-image-in-my-post-on-hugo)

## How to Set Hugo Frontmatter DEFAULT Format

create a custom template(s) in the /archetype folder
![playlist](/imgs/frontmatter.jpg)

[Solution from Github](https://github.com/gohugoio/hugo/issues/9363#issuecomment-1007392878)

## How to Setup the Hugo Search Page
![search page](/imgs/hugosearch-Screenshot%202024-06-26%20at%2022.59.25.jpg)
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