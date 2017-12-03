---
layout: post
title:      "Rails: Convention over Configuration"
date:       2017-12-03 03:01:25 +0000
permalink:  rails_convention_over_configuration
---



Rails is built around the idea of “convention over configuration.” It takes the ideas of sensible defaults and the principle of least astonishment in user interface design and extends it to try to make *developers* happy. Rails does a lot of the things implicitly, or to use an expression from Avi Flombaum, “auto-magically.” Starting out, this was something that I had to learn to accept and grew to enjoy.

Why did I have to learn to accept all the work Rails could do for me? Well I like to write code that reads the way it works [like the Zen of Python's](http://en.wikipedia.org/wiki/Zen_of_Python) principle "explicit is better than implicit." Rails does so much work behind the scenes that it felt to me like the code didn’t fully express what it is actually doing.

I promise we’ll get to the part where I enjoy Rails. 

According to the creator of Rails, David Heinemeier Hansson, [“There are so many conventions in Rails that a beginner doesn’t even need to know about, but can just benefit from in ignorance. It’s possible to create great applications without knowing why everything is the way it is.” ](http://www.google.com/search?q=David+Heinemeier+Hansson&rlz=1C5CHFA_enCA755CA755&oq=David+Heinemeier+Hansson&aqs=chrome..69i57j0l5.382j0j7&sourceid=chrome&ie=UTF-8) This threw me off at first. IGNORANCE!?!? I don’t want to be ignorant of my code.  I like knowing the smaller details and the answers to ‘how’ and ‘why’. So dealing with rails magic was startling at first. But really when you look at it rails is a predictable place. And learning how and why all the magic happens is possible (eventually).

Once you buy into the Rails philosophy life as a dev gets easier. Rails is made in an attempt to decrease the number of decisions that a developer using the framework is required to make. Conventions make code life predictable. You can depend on the Person class mapping to people table, and that it will use the same inflection to map an association of has_many :people to look for a Person class. All this done for you unless you decide to overwrite the Rails conventions. This predictability and convention makes following another developers Rails code a breeze. And fewer decisions on the things that every app has in common, in particular its default project file and directory structure, leaves a Rails developer more bandwidth to make decisions on the things that make their app different. 

Starting with Rack and Sinatra before using rails helps to understand a lot of what is happening if you do want to know more about how Rails automatically does so much. And rails can generate a lot of code, so knowing when it may be doing more than you need is important to keep your application from having a lot of unnecessary auto-magical Rails generated code.


