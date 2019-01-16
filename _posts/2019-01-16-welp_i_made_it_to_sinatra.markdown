---
layout: post
title:      "Welp, I made it to Sinatra!"
date:       2019-01-16 05:04:05 +0000
permalink:  welp_i_made_it_to_sinatra
---


And to its final project, yay! The idea I chose consists of  a CMS for a Event Planner company; this Web App will allow a planner to sign up/sign in to add, edit, delete or view all of their events, and to also see all events from all users.

**The deets...**

* I created the file structure using the [Corneal Gem](http://https://thebrianemory.github.io/corneal/); it was easy to use and fun to tweak around.
* **Schema:** A **planner** has a username and a password. An **event** has a date, a planner, a host, a budget and a category. A **category** has a name. All migrations were made using the create migrations Rake task.
* **Associations:** A **planner** has many events and many categories through events. An **event** belongs to a planner and a category. A **category** has many events and many planners through events.
* I created two controllers: The **planners_controller** and the **events_controller**. In the planners_controller are listed all the RESTful Routes with the corresponding controller CRUD actions that allow a user to view and fill out sign up and sign in forms, and to view a specific planner's events. In the events_controller reside the actions to create, edit, delete and show an specific event, or all of them.
* The **views** available are those to display the homepage, sign up form, sign in form, create new event form, edit an event form, show a specific event, a list of all events, a list of all events that correspond to a specific planner, and the layout for all other views.

Motivated by all the learning I got to experience in this project, I joined the #100DaysOfCode challenge on Twitter, where I documented the highlights and the not-so-bright moments in my way to building up this app.  You can see them [here](http://https://twitter.com/wendisha).

And if you would like to see the video demo for this application, click [here](http://https://youtu.be/XkM3RwwNyQQ).

