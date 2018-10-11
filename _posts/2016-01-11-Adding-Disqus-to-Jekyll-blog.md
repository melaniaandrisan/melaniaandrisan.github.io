---
published: true
layout: post
date: "2016-01-11 20:35:13 +0200"
categories: jekyll update
title: "Day 2 - Adding Disqus to Jekyll blog"
---




Today I managed to add Disqus to my blog. Is a prety easy step to make my play static blog a liitle bit dynamic.

I just went directly to disqus.com and after a couple of logins I ended up at [this publishers page](https://publishers.disqus.com/engage) and "started to engage".

I just loged in, added my blog name and them did some small coding:

1. I created a [comments.html](https://github.com/melaniaandrisan/melaniaandrisan.github.io/blob/master/_includes/comments.html) page in the `_includes` folder.

2. I added <pre><code>{% include comments.html %}</code></pre> in [_layouts/default.html](https://github.com/melaniaandrisan/melaniaandrisan.github.io/blob/master/_layouts/default.html)

3. Push to git... and voila :)
