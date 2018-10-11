---

published: true
layout: post
date: "2016-02-01 23:30:10 +0200"
categories: DNS
title: "Setting up a custom domain to my blog"

---

And now my blog is not melaniaandrisan.github.io anymore is mela.ro ... Yeeey:)

What I had to do was to fallow the steps from [github help](1). And in a phrase this is what I did:
I already used [cloudns](2) as cloud server so I just needed to configure the `A` record and the `ALIAS` and to create a file in my repository named `CNAME` with just a single line `mela.ro`.

Done!

To learn more about DNSs have a look on [Google support](3) page.

P.S. I started adding the links at the end page and have them referenced in the blog post.

[1]:https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/
[2]:https://www.cloudns.net/
[3]:https://support.google.com/a/answer/48090?hl=en
