---
layout: post
title:      "Vertical Slices and a Minimum Viable Product"
date:       2017-11-13 23:44:16 +0000
permalink:  vertical_slices_and_a_minimum_viable_product
---


In math we learned to rely on the order of operations. In writing code I’ve been thinking more about how the order I approach things and how that affects the outcome. Unfortunately, there are a lot of opinions on the best workflow for a developer. In math, you know to first do exponents and roots, then multiplication and division, and lastly, addition and subtraction. In primary school most people are taught PEMDAS (Please Excuse My Dear Aunt Sally) an easy way to remember the order. I don’t have a mnemonic yet for how to build an app with Sinatra, but I am starting to develop my own order of operations.

After pushing through these labs and getting to my Sinatra portfolio project for Flatiron School, I was still struggling to piece together the big picture. Conceptually, I understood the ideas, but the process of tackling things was an issue. So I took a moment to evaluate how to work more efficiently and to keep the scope of my immediate tasks manageable.

My workflow was like a pyramid. I wanted to get the major foundation completely done. So I began by building my objects and database. I got them to collaborate the way objects like to do and then I built my site from there. This worked okay but when I finished one level, there was nothing connecting it to the next. I had a huge task of connecting the last level of code to the new one. Tackling the connections of the whole model to a nonexistent controller that had no views got messy quick.

I decided to start again from scratch, but instead of building from bottom up, I took a vertical slice approach (See diagram).

![](http://www.g67.com.au/wp-content/uploads/2015/06/mke-agile-032014-slicing-the-cake-user-story-decomposition-4-638-460x321.jpg) 

I took a more agile and test-driven approach. I wanted to see what my site would be producing as I built it, continually iterating with new features. So I just built an initial class for my model to get started. Then I started designing my controller routes that connect with the model. And quickly jumped over to making views to see it all work together. And right away, I have a working site. And I let that dictate what I need to do next and fill in the blanks. Alright! I need to go back to my model and give it a base for data... a database.

As much as I like the cake analogy I send you back to my new approach on the old pyramid outlook on programming (see below).

![](http://dootrix.com/wp-content/uploads/2016/02/MVP.png)

Now the way my site is growing is a more organic process. And best of all I can really test how it works continuously. Before, at this point I just had data with no way to view it and testing it was just making assumptions of what I needed and hoping that it would be correct later. Thinking into the future like that is great, and I still like to do it, but as a newer developer getting constant feedback on your predictions is important so you can spend less time writing bad code.
This approach has a drawback if you aren’t careful though. The concept I try always be aware of while working like this is making my program open to extension/ closed to modification. So when writing code, always keep in mind that you want to allow your program to be expanded without having to modify the base code.

