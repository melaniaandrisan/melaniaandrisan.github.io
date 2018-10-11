---

published: true
layout: post
date: "2016-06-07 23:30:10 +0200"
categories: [archive, Angular]
title: "NodeJS, Angular, Express and Oracle DB"

---

In the past few weeks I was busy building a NodeJS app using Angular, Express and Bootstrap connecting to an Oracle DB and using [PassportJS][PassportJS] to authenticate the users using a adfs strategy.

Here are the most important things we wanted to cover with  it:
- separation of concerns – for the moment the applications are built using plsql which means that all the code is in the Oracle DB. The goal is to have the DB for the data storage, the nodeJS API to expose just the needed data from the table and a frontend to be able to do CRUD and display report and charts and some other things like map, calendar…
- To reuse as many logic as we can from plsql - node-oracledb gives us this possibility
- The chosen technologies should offer rapid application development – and choosing node, express and angular made this possible
- Authentication with haufe credentials – seting up a adfs passportjs strategy  made it easy
- Have the application modular – every MIWH app can be its own app using a starting project
- Offer a nice UI without spending ages building CSS – and here bootstrap with the AdminLTE helped a lot

In case you are curious how PassportJS works you can have a look at [Understanding passport.js authentication flow][flow].
To build the authentication I followed [this][auth]. And a nice article about [token base auth][token base auth].
I am building a SPA and using [ng-view][ng-view]. And to be able to create routes I used [otherwhise][other tutorial].

The App:
- I connect to Oracle Db using node-oracledb.
- The server is node.js with Express.
- The frontend is Express, Angular and Bootstrap. And the UI template is Jade.
- Creating a single page app following a similar approach with [scotch.io][scotch.io]
- Have async calls using promises
- I am using the AdminLTE theme and Fusion Charts.
- To have better [table pagination][pagination] I choose.
- And for [navigation][nav-tree]
- For the login I am using passport.

[PassportJS]:http://passportjs.org/
[scotch.io]:https://scotch.io/tutorials/single-page-apps-with-angularjs-routing-and-templating
[nvm]:https://github.com/creationix/nvm
[flow]:http://toon.io/understanding-passportjs-authentication-flow/
[ng-view]:http://www.tutorialspoint.com/angularjs/angularjs_views.htm
[other tutorial]:http://blog.kevinchisholm.com/angular/angular-js-basics-routes-part-iii-creating-a-default-route/
[auth]:https://www.ctl.io/developers/blog/post/build-user-authentication-with-node-js-express-passport-and-orchestrate
[token base auth]:https://scotch.io/tutorials/the-ins-and-outs-of-token-based-authentication
[nav-tree]:http://nickperkinslondon.github.io/angular-bootstrap-nav-tree/test/bs3_ng120_test_page.html
[pagination]:https://github.com/michaelbromley/angularUtils/tree/master/src/directives/pagination
