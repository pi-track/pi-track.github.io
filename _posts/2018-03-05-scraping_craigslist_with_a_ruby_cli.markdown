---
layout: post
title:      "Scraping Craigslist with a ruby CLI"
date:       2018-03-05 12:17:15 +0000
permalink:  scraping_craigslist_with_a_ruby_cli
---

I have a problem - I check craigslist every day for [bikes](https://philadelphia.craigslist.org/search/bik?postedToday=1&search_distance=2&postal=19147) for sale in my zip code and I end up buying one more frequently than I'd like to admit. I currently have 2 bikes in my apartment, another older beat up one which I leave outside, and a few strays floating around the city that I've pawned off on family and friends. So as I started thinking about a potential CLI project, scraping craigslist came to mind even if spending more time looking at bikes I don't need and don't have the money for was a little risky. 

I originally conceived the app as performing a few simple functions from the user perspective. I should be able to define a search or select a default and then the CLI should return a list of search results. I should then be able to select a bike from the list and get some more info on that specific bike. I realized pretty quickly that it didn't make sense to limit myself to bikes, the general category of an item makes much more sense. Unfortunately at that point I had already namespaced everything out with "bikes" showing up in classes, methods, puts, etc.. throughout my code. So I continued with bikes until I had it working and then I decided to see what it would take to get re-factor the app to scrape for items generally. It wasn't bad! I had done a good enough job separating concerns that I didn't have to do much beyond change names to be able to search for an item in general through the CLI. 

Moving through the design and construction was a learning experience and I took a few lessons away from building my first gem. 

### 1. Figure out the overall stucture first

   I realize now that I was overeager to get started on this project. Looking back - there were a few problems I ran into that some thinking and googling and a closer look at the learn curriculum would have prevented. I'm working on finding the balance between planning out my code and diving in and writing. There is a natural tension in building anything between trying to get it done and trying to get it perfect. You'll never get it perfect and if you try you'll never get it done. We've all heard the cliche "don't let the perfect be the enemy of the good." On the flip side if you don't figure out the blueprint of what you're building, what tools you'll be using, what you want it to do when you're done, you're not likely to have much success. And if you're going to do something - its always nice to do it well. 

### 2. Move fast, but deliberately

   There is a low risk to doing something wrong in software development, after all you can always back up or start over and no one dies when you get an error message. (If those assumptions aren't true then you're probably doing something wrong.) That enables you to take a pretty aggressive stance towards moving forward through problems. The speed is one of my favorite things about code - the feeling of quickly attacking a problem and getting results is exciting and a little intoxicating, but it is also dangerous. Moving too fast can easily lead to hairballs in your code that take more time down the road to untangle. I'm learning that part of the craft is figuring out the balance. 

### 3. Strike a balance

   So what does that balance look like in writing software? There is no perfect answer to that question, it's a fundamental tension, but there are definitely some best practices and ways to attack problems that can lead to better outcomes. I don't pretend to have this figured out by any means but it is something I'm hoping to get better at while at Flatiron. One of my inspirations is the way Avi codes - he's always thinking out loud and being very explicit about 'where he is' in the code. He always explicitly defines what he knows and what he doesn't. I've found that talking out loud is a good tool for figuring out where I am and what I need to do next. Talking forces you to be explicit about what you really know and what you don't, and that often makes it obvious where you need to go next. I had this experience when I was recording a code session - it feels a little magical when you go from stuck to un-stuck just by talking! 
	 
### 4. Get 'good enough' and iterate

   Another useful habit is to always be aware of "what you are doing" and to frequently ask yourself, "is this what the project needs?" In any project there are a ton of problems that need to be solved and some are more fun than others. Tweaking a regex or writing a more precise css selector can be fun but at a certain point there are diminishing returns to working on it and it can become a time suck which prevents you from moving forward. One way out is to write something 'good enough' and then move on to the next problem, with the awareness that you'll come back later and make it better when you need to.  

