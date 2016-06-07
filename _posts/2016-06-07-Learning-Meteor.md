---

published: true
layout: post
date: "2016-06-06 23:30:10 +0200"
categories: Meteor
title: "Learning Meteor"

---
Last week I spent a couple of days understanding and trying [Meteor][Meteor]. And... it has an
incredible amount of documentation on different levels.

[Tutorials][tutorials] for beginner, [videos for intermediate][intermediate Meteor]
a complete [guide][guide] and the [API documentation][api].
>
>Meteor is a full-stack JavaScript platform for developing modern web and mobile applications. Meteor includes a key set of technologies for building connected-client reactive applications, a build tool, and a curated set of packages from the Node.js and general JavaScript community.
>
> - Meteor allows you to develop in one language, JavaScript, in all environments: application server, web browser, and mobile device.
- Meteor uses data on the wire, meaning the server sends data, not HTML, and the client renders it.
- Meteor embraces the ecosystem, bringing the best parts of the extremely active JavaScript community to you in a careful and considered way.
- Meteor provides full stack reactivity, allowing your UI to seamlessly reflect the true state of the world with minimal development effort.

From the architecture point of view it covers almost all the topics that you can think of:
- separation of client and server, but the developer is not noticing the difference between them if the 'autopublish' package is added.
- the communication between client and server is done using [publish subscribe][publish subscribe]
- the [application structure][application structure] is easy to use and offers flexibility. the only real constrain is:  _to the new module system code must be placed inside the imports/ directory in your application._
- it follows a [coding style][coding style] and you can enforce it in your project tool
- supports different UI templating engines: Blaze, Angular, React.
- it has an incredible amount of packages build buy the team or by community and you can get them from npm and Atmosphere.  
- they cover a lot of topics regarding [security][security] and offer best practices
- the [deployment and monitoring][deployment] is easy and fast and we can use different settings for dev, staging, live.
- it uses MongoDB but there are different packages that make possible building an App using Meteor with [Oracle][oracle] or with [Postgres][Postgres].

Other cool stuff:
- [optimistic UI][optimistic UI]
- [Methods][methods security] which help with [security][methods security] too


[Meteor]:https://www.meteor.com/
[tutorials]:https://www.meteor.com/tutorials/angular/creating-an-app
[intermediate Meteor]:https://www.meteor.com/
[guide]:http://guide.meteor.com/
[api]:http://docs.meteor.com/
[application structure]: http://guide.meteor.com/structure.html
[coding style]:http://guide.meteor.com/code-style.html
[packages]:http://guide.meteor.com/atmosphere-vs-npm.html
[security]:http://guide.meteor.com/security.html
[deployment]:http://guide.meteor.com/deployment.html
[publish subscribe]:https://docs.meteor.com/api/pubsub.html
[oracle]:https://atmospherejs.com/metstrike/meteor-oracle
[Postgres]:https://meteor-postgres.readthedocs.io/en/latest/
[optimistic UI]:http://info.meteor.com/blog/optimistic-ui-with-meteor-latency-compensation
[methods security]:https://www.meteor.com/tutorials/angular/security-with-methods
