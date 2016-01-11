---
published: true
---


## Day 2 - Adding Disqus to Jekyll blog

Today I managed to add Disqus to my blog. Is a prety easy step to make my play static blog a liitle bit dynamic.

I just went directly to disqus.com and after a couple of logins I ended up at [this publishers page](https://publishers.disqus.com/engage) and "started to engage".

I just loged in and I ended up at this page:

![Screenshot 2016-01-11 21.06.23.png]({{site.baseurl}}/_posts/Screenshot 2016-01-11 21.06.23.png)

Easy to fill in and the next steps ware:
1. I created a [comments.html](https://github.com/melaniaandrisan/melaniaandrisan.github.io/blob/master/_includes/comments.html) page in the `_includes` folder.
2. I added `{% include comments.html %}` in [_layouts/default.html](https://github.com/melaniaandrisan/melaniaandrisan.github.io/blob/master/_layouts/default.html)

3. Push to git... and voila :)
