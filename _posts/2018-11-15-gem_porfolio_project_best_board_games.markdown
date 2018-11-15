---
layout: post
title:      "Gem Porfolio Project: Best Board Games"
date:       2018-11-15 23:01:47 +0000
permalink:  gem_porfolio_project_best_board_games
---


[Best Board Games project](http://https://github.com/renojames/best_board_games)


Since what *did* work in the project will be evident in reviewing it, I am going to spend this blog post detailing how I was unable to fulfill my original ambition for the app, and how I had to retool my goals several times. 

I decided to create a CLI that would scrape the ranked board games from BoardGameGeek.com and return them to a list, from which the user could then select a specific game to view details of note. The user would be able to view lists of games of different lengths using a looping logic. 

The program primarily scrapes Board Game Geek's [ranked list of board games](http://boardgamegeek.com/browse/boardgame), iterating over the CSS selectors for each game (row) in the table and grabbing basic data from the child elements.

However, the information found on the list page isn't particularly interesting; it doesn't include a description of the game, play time, number of players, or genre information. So, my plan was to do an embedded scrape of each game, storing the link for each game as an attribue of the game, using open URI to get into the game's individual page, and then scraping additional data to be added as attributes to the game's specific hash. This would all be wrapped in the single iterative scrape for a given game's row. 

I quickly ran into a problem; once I had scraped my way into the specific page for a given game (example: [Gloomhaven](http://boardgamegeek.com/boardgame/174430/gloomhaven)) I found that Nokogiri was not returning any values using the CSS selectors I was choosing based on developer tools, for reasons that were not immediately clear to me. 

I spend a *lot* of time trying to find CSS selectors that would respond in Nokogiri, to no avail. 

Eventually, I used Postman to view the HTML of the game's page after a call, and discovered that Board Game Geek renders their individual game pages using Angular, which was Greek to me and not condusive to scraping with Nokogiri. After that plan went out the window, I tried to open each game's individual Amazon page as linked from the main list, but ran into similar problems, with Nokogiri not recongizing the CSS selectors as they appeared in developer tools. 

My final project simply scrapes information from the main list of board games, without attempting any imbedded scrapes. I'd like to learn more about Angular and JSON to do more complex scraping functions in the future. 



