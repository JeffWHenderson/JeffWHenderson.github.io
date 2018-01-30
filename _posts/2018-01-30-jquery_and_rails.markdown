---
layout: post
title:      "JQuery and rails"
date:       2018-01-30 21:20:45 +0000
permalink:  jquery_and_rails
---


Turbolinks makes navigating your web application faster. It is supposed to behave with the speed of a single page application without the added complexity of a client-side Javascript framework. It uses HTML to render your views on the server side and automatically fetches and swaps its \<body\> and merges its \<head\>, all without the time waste of a full page load.

It's a great tool and DHH is a big fan of turbolinks but it can cause some very hard to find bugs. I just couldn’t figure out what was going wrong with my rails app built with a jQuery frontend. I debugged everything i could possibly imagine in my code. Refactoring in every which way and I still had the same issue...  

I was retrieving data from an API I set up and updating the page with content from my API. But when I clicked the link the javascript was not working properly. The first time I clicked it I was sent to an entirely different page filled with my ugly JSON data. The app is supposed to fetch that info and render it directly on the current page. It shouldn’t go to the endpoint! 

The first thing that comes to mind is preventDefault(). Did I forget to do that? No, everything looks good there. And even more difficult to understand is after going back to the original page and clicking the link it would work properly. So why is preventDefault() not working the first attempt but it works fine after that?

I had a 30 minute debugging session with a more experienced developer. Pairing with others is a great way to learn and increase productivity. I took the role as driver in the pairing session and the navigator did just that, helped me go down the proper direction to find a solution. My program was still just as broken after the session but I was armed with lots of blog post to read and a route to solve my problem.

My solution ended up being to remove the Turbolinks gem, which also required taking references to it out of the javascript manifest and the layout HTML. That is all it took! Something rails put in my app for me was causing the issue the whole time. 

This got me thinking about my understanding of rails. As a rails developer, I have to become familiar with all the gems that come with rails because so many things are working together. Know your gems, because even ones you haven’t installed yourself are still part of your program and errors can come from anywhere in the program.

