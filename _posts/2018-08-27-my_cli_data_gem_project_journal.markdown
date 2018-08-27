---
layout: post
title:      "My CLI Data Gem Project Journal "
date:       2018-08-27 04:28:30 +0000
permalink:  my_cli_data_gem_project_journal
---


A long journey is about to be described day by day, so please bear with me (I'm a part-*part*-time student, that can barely put 2 or 3 hrs a day into this).

**Day 1:** Read [the instructions](https://learn.co/tracks/full-stack-web-development-v6/object-oriented-ruby/final-projects/cli-data-gem-project) to get my project started. Began brainstorming about what would be an awesome and useful topic to work with. My first choice was to create a CLI that would allow a user to get a list of blood donors by entering their zip code and/or blood type. Well, that didn't work since I could not find a website that listed this information for the United States. I ended up choosing to talk about my daily booster... Coffee <3

![](http://media.graytvinc.com/images/810*455/Cup+of+Coffee.jpg)

**Day 2-4:** The search for an informative website began. Chose [this one](http://www.cafepoint.co.uk/different-types-of-coffee/). I filled up my CLI Project Mode Ideation! Form, and chose my project's name, **TodaysCoffeeCLI**. I watched [Avi's Video Walkthrough](https://www.youtube.com/watch?v=_lDExWIhYKI) which is very detailed and helpful, proceeded to create my new gem with bundler and completed the In-Browser IDE Setup which gave me a hard time for the following 2 days: I named my gem incorrectly and for the sake of my OCD I needed it to match my repository's name. After a few failed atempts to delete the gem, I finally got it working deleting the Sandbox repo, and started off fresh. Made my second commit adding the executable file and giving the OS the required permissions to allow a user access to **todays_coffee_cli** through bash.

**Day 5-7:** Third commit: created my CLI Controller (which still needs some improvement). By the way, I forgot to add before that after submitting my Ideation Form, they told me the website I chose would be tricky to scrape, and boy! were they right! The info is not very well contained: a "p" tag contains practically all the info I need, so it became  a little hard to get specific pieces of data when needed. Scheduled my first 1:1 session with a tech coach, it was so helpful!


**Day 8-9:** By now I must have like 40 commits, since I am working from the In-Browser IDE I need to advoid losing any bit of progress. Created my Coffee model, which serves as the scraper for the program. I refactored the scraper method a lot of times, finally settling for what looked more dynamic, or the best I could get from the chosen website. I also refactored my CLI to advoid using a loop to exit, now the greeting method is a bit more sequential.

**Day 10-11:** Finally started seeing an improved version, closer to what I had originally envisioned. Recorded my video demo showing how the user interacts with the gem. Finished this blog post and submitted my checklist.

Click [here](git@github.com:wendisha/todays_coffee_cli.git) to see my gem's repository.
Thank you for reading!
