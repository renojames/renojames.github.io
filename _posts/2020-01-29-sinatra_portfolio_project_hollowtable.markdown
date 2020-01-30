---
layout: post
title:      "Sinatra Portfolio Project: HollowTable"
date:       2020-01-30 02:10:23 +0000
permalink:  sinatra_portfolio_project_hollowtable
---


**The Concept**

When my friends and I get together on the weekends, we board game. Large group games, euro games, role-playing tabletop games; we are nerds. 

So, for my Sinatra Portfolio-slash-CMMS project, I wanted to design a simple application that would function like a Goodreads for board games. You could add games to and remove games from your library, edit the game records, and leave comments alongside other users. However, there is an important conceptual difference between Goodreads and my application, which I chose to call HollowTable: Goodreads gets its data from - I assume - a database of book records based on each book's ISBN number. In HollowTable, when a game doesn't already exist, it's up to the user to add it to the database. 

Once a board game is created in the application, any user who has added the board game to their library can edit all the properties of the game - genre, description, summary, etc. The board game's title cannot be edited, since it is intended to be the user-facing constant representation of the game itself. 

I found this crowd-sourced, CMMS-meets-social network concept interesting, but it poses several problems that I didn't solve in my project. What if someone creates a fake game, or enters a game's title incorrectly? What if someone uses the European spelling for an existing board game's name, creating a duplicate record? The solution would be to have admins or superusers responding to tickets entered by users, with more complex automation skimming the database looking for bad or fake data entered by trolls or bots. Since the goal of the project was to create a Sinatra-based MVC-CRUD application, I didn't get into all of that in the code, but it is something that I keep in the back of my head should I choose to expand the project in the future. 

**The Setbacks**

For what it is, this project took me a long time to finish. I mean, a really, really long time. 

My progress through Learn.co has always been slow, since I made the decision to commit to the program while still working a full-time job. But several roadblocks hindered me more than I would have liked. 

The first was my coding environment. Before this project, I had alway worked in the Learn IDE, opening assignment and projects directly from Learn.co. I felt a little hamstrung by this, a little lacking in the basics, since Learn's gooey was doing all the overhead work needed just to get going on writing code. I decided that setting up my own coding environment for this project would be a good learning experience, and it was. Choosing an editor, getting a shell running, installing all of the languages that the Learn IDE had streamlined for me, plugging it into git and Github, and making it all work together helped me wrap my brain around all the moving pieces of the code writing and revision process in a way I hadn't appreciated before. It also took *forever*, which discouraged me, and caused me to drag my feet. But I eventually got it going. 

Then, I ran smack-dab into a hand injury, the kind that required surgery. Before surgery, typing for my nine-to-five was hard enough, and by the time I got home I was in enough pain that I couldn't bring myself to do any more computer work. After the surgery, a fun 12-week recovery began, during which I didn't get any work done on the project. Even after my hand was back in action, the guilt and feel-bad of not having made any progress on the project paralyzed me, and I found myself dragging my feet to get going again. 

Eventually, I made myself sit down and get re-acquainted with the code. I remembered that it was actually fun to create something, and picked up enough steam to get over the finish line with something that, I think, satisfactorily meets the project requirements. 

**The Product**

I am reasonably proud of the very simple app that I wrote. It's not pretty - I chose to forgo any pre-set stylesheets and instead created a bare-bones one myself - but it is functional and, I think, readable. If I had infinite time and resources, I would implement some of the ideas mentioned in the opening of this post, as well as a few others - a "rivals" functionality, like other social media networks have friends; the ability to see who else in your geographical area owns the same games as you, or is interested in meeting up for game night; etc. 

For now, I'm just happy I saw it though to the end. 
