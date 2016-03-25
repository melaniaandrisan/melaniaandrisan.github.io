---
published: true
layout: post
date: "2012-09-30 23:35:13 +0200"
categories: archive
title: "Instagram API and OAuth 2"
---


In the previous post I had a small presentation about REST API. I learned how to build it and to use it but I wanted to know more. So I started looking for a new challenge and it came from [Instagram API][1]. They have a lot of endpoints to use and also an authentications process. They are using the OAuth 2 protocol. [Here][2] we can find the entire documentation for OAuth 2. In small lines the in OAuth 2 has 4 components:

- resource owner - An entity capable of granting access to a protected resource. When the resource owner is a person, it is referred to as an end-user.
- resource server - The server hosting the protected resources, capable of accepting and responding to protected resource requests using access tokens.
- client - An application making protected resource requests on behalf of the resource owner and with its authorization.
- authorization server - The server issuing access tokens to the client after successfully authenticating the resource owner and obtaining authorization.

And here is the communication between them:

![Oauth2][3]

After we have the token we can make the secure requests via https.

In my application I want to take the Popular Photos, My Photos and Friends Photos. To make this possible I need to connect to the next endpoints:

- Popular Photos

GET: /media/popular

https://api.instagram.com/v1/media/popular?access_token=ACCESS-TOKEN

- My Photos:

GET:/users/self/media/resent

https://api.instagram.com/v1/users/self/media/resent?access_token=ACCESS-TOKEN

- Friends Photos:

GET: /users/self/feed

https://api.instagram.com/v1/users/self/feed?access_token=ACCESS-TOKEN

In the previews post we have connected to our web API service but without authentication to it. Now that we have all what we need from Instagram API we will use it from Backbone in the next Posts. Before doing this I will create a new project using ASP .NET MVC and jQuery Mobile and I will see what is actually jQuery Mobile and how I can use.

[1]:http://instagram.com/developer/endpoints/
[2]:http://tools.ietf.org/html/draft-ietf-oauth-v2-12
[3]:{{ site.url }}/assets/Kindle.jpg
