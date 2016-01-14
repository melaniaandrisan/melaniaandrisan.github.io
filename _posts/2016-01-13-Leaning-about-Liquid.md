---
published: true
layout: post
date: "2016-01-12 23:35:13 +0200"
categories: liquid
title: "Day 4 - Learning about Liquid"
---

A short day today. I started looking at [Liquid](https://github.com/Shopify/liquid) and see what I can do with it and how.

What I first learned about **Liquid** on [Shopify](https://docs.shopify.com/themes/liquid-documentation/basics) documentation is:

>Liquid is an open-source, Ruby-based template language created by Shopify. It is the backbone of Shopify themes and is used to load dynamic content on storefronts.
>
>Liquid uses a combination of _tags_, _objects_, and _filters_ to load dynamic content. They are used inside Liquid template files, which are a group of files that make up a theme.

#### Tags

>Liquid tags are the programming logic that tells templates what to do. Tags are wrapped in: <code>{ % % }</code>. (if, for, ...)

#### Objects

>Liquid objects contain attributes to output dynamic content on the page. For example, the product object contains an attribute called title that can be used to output the title of a product.
>
>Liquid objects are also often refered to as Liquid variables.
>
>To output an object's attribute on the page, wrap them in <code>{ { } }</code>

There is also a list of global objects described in the [documentation](https://docs.shopify.com/themes/liquid-documentation/objects).

#### Filters

>Filters are simple methods that modify the output of numbers, strings, variables and objects. They are placed within an output tag <code>{ { } }</code> and are separated with a pipe character |.

Another nice documentation is on [github](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers).

P.S. For the moment I have some problems with the `code` tag.
