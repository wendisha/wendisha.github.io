---
layout: post
title:      "Virtual Blood Bank"
date:       2019-04-25 01:54:25 +0000
permalink:  virtual_blood_bank
---

A platform that makes it easier to donate or request blood donations, has been an idea I've been pondering for previous Portfolio projects, and finally gave it a go for the Rails section one. Initially, I wanted to allow a user to sign up to the app as donor or a recipient. Somewhere along the way, for time management purposes I decided to simplify the initial structure of the app, and stubbed out the following associations:


![](https://i.imgur.com/sA0VMid.jpg)


A donor, the user of the app, has many appointments, and many clinics through appointments.
A clinic, who acts as the recipient for now, has many appointments, and many donors through appointments.
An appointment belongs to a donor and a clinic. The writtable attribute for this join table is the date for said appointment.

At first, [the list of requirements](https://learn.co/tracks/full-stack-web-development-v6/rails/rails-project-mode/rails-portfolio-project#requirements) for this project seemed very intimidating, but once I dove into it, and approached it one by one, it all started to make sense:

* To start off the app, I used the  `rails new`  command to create the basic file structure. Then used generators to create the models and missing migrations.

* For styling and general formatting of the pages, I resorted to [Bootstrap](https://getbootstrap.com/).

* To seed the database with fake data to test around, I used the [Faker](https://github.com/stympy/faker) gem.

* To meet the nested routes requirement, I implemented two, both render the new form and redirect to the show page for an appointment, one is nested under donor/:id, and the other one under clinics/:id. 

* Showing validations errors was a little tricky at first, but thanks to [this Avi's lecture](https://learn.co/tracks/full-stack-web-development-v6/rails/rails-review-todomvc-2/todomvc-2-lists-have-items?batch_id=306&track_id=43149), I was able to get it done. 

* Implementing OmniAuth was definitely a challenge. Since we've worked with the Facebook strategy, I chose it for my app, and finally got it working after lots of reading, and a long and productive pair-programming session. 

* Study groups were **key** to get me and keep in on the right track.

What I loved the most about this project, is that I finally worked on an idea I can see myself coming back to, to keep working on it and making it better, as I learn new things and earn new skills.


