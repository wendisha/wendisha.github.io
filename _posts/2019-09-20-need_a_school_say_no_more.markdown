---
layout: post
title:      "Need a school? Say no more!"
date:       2019-09-20 22:25:51 -0400
permalink:  need_a_school_say_no_more
---


When deciding on a project idea for this, my final project for Flatiron School's online Software Engineering program, I really wanted to work on something I could use myself, like, for real! And I remembered that my oldest will be starting kindergarten next year, so the choice became obvious: I need an application that will make the process of choosing schools an easier task.

Find My School is a web application that allows users to create an account and search for schools by zipcode. Then, a logged in user also has the ability to bookmark those schools of their interest. As of now, it consists of three models: User, Bookmark and School, where  `bookmarks`  is the join table for  `users`  and  `schools`.

Starting the app:
1. Two GitHub repositories were created; one for the front-end and another one for the back-end of the application.
2. The initial file structure of the front-end was created by running the  `create-react-app`  command.
3. The initial file structure of the back-end was created by running the  `rails new`  command, with the [`--api`](https://guides.rubyonrails.org/api_app.html) flag.
4. Nested the users, bookmarks and schools controllers inside  `/api/v1` to follow convention and best practices, where  `v1` represents the first version of this Rails API.

Issues I encountered and lessons learned:
* Deciding on the structure of the app, was no easy task, but I highly suggest working on associations as precisely as possible before jumping to the code.
* Learned that "type" is not to be used as a column name in Rails, because it uses this to define the subclass of a model that should be loaded. But [here's](https://mattconnolly.wordpress.com/2012/06/01/rails-beware-a-column-named-type/) a work around should you need to still name it that way.
* I got a lot of great guidance by watching the Globetrotter Project Build series, by Howard DeVennish (available on [Learn Instruct](https://instruction.learn.co/student/home), where he used [Netflix/fast_jsonapi](https://github.com/Netflix/fast_jsonapi) as a serializer. I had experience with Active Model Serializer, which I believe is easier to work with, but still decided to learn how to use this one, and after reading a lot from it's documentation, I was able to get it working.
* The original API I chose to search for schools ended up being outdated and responds with XML, not JSON. I could've pased XML using a package such as [xml2js](https://www.npmjs.com/package/xml2js), but I decided to switch APIs, not only for this reason, but the other one was also providing limited access, time wise. 
* When a user bookmarks a school, the school needs to be saved first and from there, also a bookmark. I tried unsuccessfully redirecting from the schools_controller create action, to the bookmarks_controller create action. Ended up instantiating a new Bookmark from the school_controller instead.

...more details will be added tomorrow, breaks are important! :)


