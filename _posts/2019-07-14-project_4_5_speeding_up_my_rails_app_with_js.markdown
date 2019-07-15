---
layout: post
title:      "Project 4/5... Speeding up my Rails app with JS"
date:       2019-07-15 02:52:17 +0000
permalink:  project_4_5_speeding_up_my_rails_app_with_js
---

![test](https://www.memecreator.org/static/images/memes/4782196.jpg)

No easy task!! JavaScript was, and still is, confusing. But thanks to various resources, including [Cernan Bernardo's videos 🙌 ](https://www.youtube.com/watch?v=oHPM0ekV7zQ) I was able to take advantage of JavaScript's interoperability, putting together various functions to make my Rails web app faster, avoiding page reloads. Said app allows users to register and create appointments in different clinics to donate blood. If you'd like to read more about it, you can do so [here.](http://wendycalderon.com/virtual_blood_bank)

The first step was to modify certain controller actions to render JSON, this was easily tested by navigating to the same route, and appending .json to it. After deciding which links I wanted to implement JS functionality on, I created the even tlisteners to satisfy the [project requirements](https://learn.co/tracks/full-stack-web-development-v7/rails-and-javascript/project-mode/rails-with-javascript-portfolio-project#requirements), i.e., rendering an index, a show, a has_many association and submitting a form through JavaScript.

* Index: render the entire list of clinics.
* Show: render a specific clinic info.
* Has_many: render the list of appointments pertaining to a specific user, on their show page.
* Form submission: submit the form to create a new appointment through JavaScript.

After taking over those events, I added  `gem 'active_model_serializers'`  to my Gemfile, and made sure   `gem 'jquery-rails'`  was also there.  I used  `fetch()`  to make the data request to my controllers, which gives us a promise that will be resolved or rejected. Since we wrote the backend API, it will be most likely resolved. For the form submission, the data entered by the user is handled with the  [`.serialize()`](https://www.w3schools.com/jquery/ajax_serialize.asp)  method and a HTTP POST request through the [ `$.post()`](https://www.w3schools.com/jquery/ajax_post.asp)  method.

**Tips:** 
* Through trial and error I realized everything that had to do with **turbolinks** needed to be removed from the app.
* Also, I used Bootstrap and had issues by having the slim min jQuery link, because it doesn't have  `$.post()`  AJAX function (I went the BootstrapCDN route); a simple change of links solved this. 
* Another important tip! Remove the coffee files or rename them to be JS, otherwise they will get loaded first. 
* And, avoid using arrow functions in your prototype functions.

I used JS constructors to create the clinics and appointment objects, and added prototype functions to format the HTML to be shown, to finally show it on the DOM.



