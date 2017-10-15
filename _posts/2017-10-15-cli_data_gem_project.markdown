---
layout: post
title:      "CLI Data Gem Project"
date:       2017-10-15 18:51:31 +0000
permalink:  cli_data_gem_project
---


The scariest thing as a new programmer is looking at a blank file. So I got to work quickly and got a functional program going. With the resources that were given to me making a scraper that communicated with a CLI was totally possible. Don’t get me wrong, I had to debug and reevaluate how things worked but really I just kept pushing code until I got a working program. 

The second scariest thing in coding, for me, is having code that works but needs to be refactored. And that’s a place i found myself. Breaking coding to fix it seems crazy but I realized my objects were taking all kinds of responsibilities.

First, I was scraping a documentary site to get a list of the categories.  And i added that info to a class variable. Something like this in pseudo code:

**@@catagories = []

**Def Scrape_categories
**	#scrapes
**	Pushes categories to the class variable categories
End

**Def self.categories
**	@@categories
end

Pretty simple.  I actually made the categories array hold more arrays each with the category name and an href attribute. This works because each sub-array can list the name in index 0 and the link for more scraping the categories' documentaries in index 1. So to get the first category I would call Scraper.categories[0][0] and its associated href would be at Scraper.categories[0][1].

I used a very similar format by adding another class variable that took in the list of documentaries from the category page (Using the url i stored in index 1 of each category).

I really loved it. Everything worked well but something didn’t feel right. There were no collaborating objects with the Scraper object i had made. I was just storing things in arrays and accessing them. By the way, I tend to error on the side of using arrays a lot.

Well now I just feel bad. I went through a whole section in the Learn program about making objects work together and I’ve only got a controller and a scraper object. I think this structure is still a more simple way of implementing the app I have in my head but the point of learning isn’t doing the same techniques you always have. So I stared at my code asking myself, “Is it worth breaking to at least try making objects collaborate together.” I almost didn’t, but I know if I’m ever going to get better at working with objects I need to get uncomfortable and push myself. 

I break my code. I scratch my head. I pace around thinking of how to fix it or just go back to how I had it before. I keep working and honestly, I think I may have gotten more understanding about objects from that refactor than any other time. Because all the pieces were in place. All the concepts have been shown to me that I need at this point. The key difference: Everything was my code. I understood everything about the program, hopefully, so the only thing that occupied my thoughts was objects collaborating. And that's really cool.

I extracted the documentary pages into a new object and my work felt more complete. The program worked exactly the same but writing better code makes you feel better. So, if you are getting ready to start your gem you should really go for it and try to make something you’re less comfortable with if you feel like it is better code.

