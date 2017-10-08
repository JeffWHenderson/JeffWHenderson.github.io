---
layout: post
title:      "Testing with colaborating objects"
date:       2017-10-08 03:03:11 +0000
permalink:  testing_with_colaborating_objects
---


Moving into the world of object orientation is a difficult change as a new developer. But why? Starting off, Object Orientation isn’t so difficult conceptually. Beginner examples of objects mirror the real world. Object examples like: a School has many students, students belong to a school, teachers also belong to a school, and a school has many teachers. At this point I’m thinking “Wow, this is going to be a breeze.”

Well, I was wrong. The metaphors are easy to understand but I let that fool me and wasn’t paying close enough attention to the new patterns sneaking into my code. I had to slow down and dive deep to get an understand of coding for object orientation and it revealed to me some gaps in my knowledge that sent me even further back. 

The biggest gap was all around how i debug. Using irb in the console works really well when you have one file to debug. When you want to check out new code you can paste your file into the new irb universe. Did you get the return you expected? No. Don’t worry, make a good guess and repeat. Irb is a great tool for debugging one object or file.

Now try to do that with 3, 4, or 5 classes.  Oops. You’ll have a lot of copy and pasting to do in your new irb universe every time you want to debug.  That's not the only problem, you have collaborating objects. The function you want to test in class A relies on instances of class B and class C. Now testing in irb isn’t working so well.

Learning to use pry more efficiently can make life easier. I had to get way more familiar with pry until i found another debug trick. Use the bin directory to run the entire program. Its good first to see the objects collaborate in real time. Setting a debug controller that bin runs gives quick feedback and I get to see the objects work in real time. Follow the tests and comparing outputs you get from running bin make debugging easier and very fun.  You get to see how your program actually runs while debugging which, for me, gives me quick insight into how my program is running and how the patterns I use are working together in the objects.  

