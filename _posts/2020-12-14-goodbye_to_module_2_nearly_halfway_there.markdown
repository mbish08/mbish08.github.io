---
layout: post
title:      "Goodbye to Module 2!  Nearly halfway there!"
date:       2020-12-15 01:47:24 +0000
permalink:  goodbye_to_module_2_nearly_halfway_there
---


Module 2 has been challenging for very different reasons than Module 1.  SQL and ActiveRecord seemed to come to me much more naturally than working with Ruby in Module 1.  So, much of the learning in Module 2 was easier to absorb.  My challenges this module were in staying caught up.  I started the module a little late, had a surgery, and some other random life events that came up.  Not to mention coronavirus which seems to be hitting me on multiple fronts.  The combination of all of these things (and more) meant I started my module 2 project later than I had hoped, but nonetheless, I got to the end!  I am determined to make it thru the entire track in one go while at the same time squeezing out as much learning as I can. 

One of the pieces of learning from this module I found most fascinating was erb (Embedded Ruby) tags.  Before starting this new chapter in my journey, I knew there were different coding languages and they needed to be able to work together to create applications.  To see how they can intermingle within one file is just amazing.  Picture it, erb tags.  You are writing embedded Ruby tags, inside of html, inside of a Ruby file.  And it works (well mostly, assuming I don't mess up the syntax)!

String interpolation is fun, but erb tags just bring that fun to a whole new level.  Let's look at a couple of examples.

Let's say I want to create a link in my program and I want it to be super flexible.  Let's take a look at this line of code from my project:

 <a href="/coffees/<%= @coffee.id %>/edit">Edit</a>
 
 This example is using the "<%=   %>" erb tag.  This tag allows you to use a variable within an html tag, thus giving you a dynamic link.  The "=" included indicates that whatever is in the middle of the tag will be visible in a user interface.  
 
 Now, let's say you don't want a user to see a certain piece of code/verbiage, but you need it for a view.  
 
 <% if @coffees == [] %>
 
This erb tag does not include "=" which means the line of code will run, but it will not be visible on the front end.  This is particularly useful when one needs to iterate to display something and you don't want/need a user to see all of the code and you just want them to have a nice clean interface to work with.  

There are many other pieces of information in module 2 that are probably way bigger than erb tags.  It just happens that this was the piece that really was the neatest item that I really enjoyed working with and learning how to use. 
