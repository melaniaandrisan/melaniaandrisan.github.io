---
published: true
layout: post
date: "2012-10-02 23:35:13 +0200"
categories: archive
title: "Backbone.js"
---


What we have till now? We have the server and the connection to it, we have the beautiful display with jQueryMobile and we have the possibility to fetch data from Instagram API, just that we did not made the login to it jet. What we will do next it will be to create a model for our photos and display a collection of them using backbone.js on the client. The collection will be fetched from Instagram API having a token in the URL. The token will be taken at the first run of the application when the user will click the Login button and will receive the token instead.

But first lets see what is Backbone and what it can do. In small words we can say that backbone changes the spaghetti code into ravioli. There are also other js frameworks which are able to do that :) , knockout, or knochback, but I chose Backbone because it is used by a number of app on the web right now like LinkedIn Mobile, WordPress, Foursquare and a lot others, you can find the entire list here. And I believe in that idea which says that good things are embraced by many and they don’t need too much marketing.

We can see Backbone like MVC architecture pattern just that C is from collection. So, we have the “Model: Express.models.Photo = Backbone.Model.extend({" ; the Collection: “Express.collections.Photos = Backbone.Collection.extend({" and the Views: “Express.views.PhotoView = Backbone.View.extend({" "Express.views.PhotosView = Backbone.View.extend({".

This are just the declarations, we can see that if we want to create a model we will need to extend from Backbone.Model and also we will do the same to Backbone.Collection and Backbone.View if we need those too.

Besides Models, Collections and Views, Backbone has also the Events, the Router and History. We can build the photo app in 2 ways: first one is to use the navigation provided by the jQuery Mobile and to navigate from page to page and load data on demand; the second one is to suspend the jQuery Mobile navigation and to use the Backbone Router to navigate basically changing the content of the main div with the one needed.

In this example i will use the Router navigation, to see how it works and which are the steps to fallow when we start with the model and we end with the router.

I created a mvc mobile app from VS and after that I added the needed reference to Backbone and a new file for js.

I’ve cleaned up the Layout page and I have there just @RenderBody in the body tag. In the end in the Index.cshtml I have just the script templates and the page definition.I’ve added all the needed code here in the html panel.

In the javascript file first we will build our namespace for backbone:

Instagram = {
models: {},
collections: {},
views: {}
};

After we have this we will go further and build our first model for Photo,  and then I did the view for it and the collection and the view for collection. And I realised that I need to do the Authentication and I created a template for it to be able to insert it into view when needed.

To be able to do this I needed a View for it and I created the AuthorizeView which takes the template from html, sends it the authorisationUrl and in the end returns the created html. To access faster the needed urls I created a config object which will return all the need paths.

Now that we have all the views we need just to display and to access them. To do this we will build the router. First we need to extend the router, just like we did withe the other Backbone components. Into the extend braces we can add the routes. We need to define the routes for home, my photos, friends photos and popular photos.

routes: {
"": "index",
"your_photos": "your_photos",
"your_friends": "your_friends",
"popular": "popular"
},

When we will call the autorize url he will come back to the redirect url with an #access_token page like in the url. To be able to take that and added in the localStorage we will set a route in the initialize function.

initialize: function () {
this.route(/^access_token=(.*?)$/, "access_token", this.access_token);
},

What we have here is: the first param which the routing regex, the second param is the route name and the third is the callback.

In the callback we will save the token is localStorage using the storage object, you will find it in the code sample.

Now that we finish with the authentications we go further and handle each and every route. For example de popular one is:

popular: function () {
$.mobile.showPageLoadingMsg();
var photos = new Instagram.collections.Photos();
photos.url = 'https://api.instagram.com/v1/media/popular?access_token=' + Instagram.storage.getAccessToken();
var view = new Instagram.views.PhotosView({ collection: photos });
$(“#main”).html(view.el);
}

In the end we just need to instantiate the router and thats it, just that it is importent to have router defined in jQuery(function ($){ } and also to suppress the navigation from jQuery Mobile in pageinit.

$(document).live('pageinit', function () {
$.mobile.ajaxEnabled = false;
$.mobile.linkBindingEnabled = false;
$.mobile.hashListeningEnabled = false;
$.mobile.pushStateEnabled = false;
});

And thats it, we have now our application running.

In the next poste we will se how we can do this with the navigation from jquery mobile.
