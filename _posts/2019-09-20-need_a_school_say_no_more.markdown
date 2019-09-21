---
layout: post
title:      "Need a school? Say no more!"
date:       2019-09-21 02:25:50 +0000
permalink:  need_a_school_say_no_more
---


When deciding on a project idea for this, my final project for Flatiron School's online Software Engineering program, I really wanted to work on something I could use myself, like, for real! And I remembered that my oldest will be starting kindergarten next year, so the choice became obvious: I need an application that will make the process of choosing schools an easier task.

Find My School is a web application that allows users to create an account and search for schools by zipcode. Then, a logged in user also has the ability to bookmark those schools of their interest. As of now, it consists of three models: User, Bookmark and School, where  `bookmarks`  is the join table for  `users`  and  `schools`.

Starting the app:
1. Two GitHub repositories were created; one for the front-end and another one for the back-end of the application.
2. The initial file structure of the front-end was created by running the  `create-react-app`  command.
3. The initial file structure of the back-end was created by running the  `rails new`  command, with the [`--api`](https://guides.rubyonrails.org/api_app.html) flag.
4. Nested the users, bookmarks and schools controllers inside  `/api/v1` to follow convention and best practices, where  `v1` represents the first version of this Rails API.

...more details will be added tomorrow, breaks are important! :)


