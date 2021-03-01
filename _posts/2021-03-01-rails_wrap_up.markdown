---
layout: post
title:      "Rails wrap up"
date:       2021-03-01 23:27:06 +0000
permalink:  rails_wrap_up
---


What a journey module 3 has been!  Tons of learning, increased time requirements at work, two very close to home deaths, and a pandemic to name a few big items that happened all in one module.  Let's talk about the pandemic for a quick second.  

Yes, I know.  No one wants to talk about the pandemic anymore.  However, one thing that was made abundantly clear was that many of us were no where near prepared for stay at home orders or supply shortages.  This inspired me to create an application that allows a user to create and update an inventory of their supply items.  This can be used to prepare for a crisis, keep a general list of every day supplies, be ready for the zombie apocalypse, or just to make sure you will never again be caught in a pandemic having to don your best tactical gear to go hunting toilet paper when it has become all but a memory.  

Now, for one of the most pain saving little tips I have discovered so far.  Have you ever been playing around with your models and database in your console only to later find that what you did is now jamming up your mojo?  Sometimes you can just reset the database and keep going but then there are those times that you really want to keep working with what you have in there and you didn't put it in a seed file and now wiping it all out makes you sadder than you care to admit.  Well, I found a solution:  'rails c -s'.  By adding the " -s" at the end, this designates the console session as a sandbox and will roll back anything you had going on and ensuring your database stays trouble free.  This was definitely a game changer.  

Another useful item of note is partials in views.  Partials are great for lots of reasons.  They can help keep your code DRY and also reduce the possibility for errors.  Here is an example:  new and edit forms.  Often, your new and edit forms in a view will be almost identical.  Here is a sample of a new form for Purchase.  The edit form looks exactly the same.   

<%= form_for @purchase do |f| %>
    <%= f.label :quantity, "Quantity of supply:" %>
    <%= f.text_field :quantity %>
    <br>
    <%= f.submit %>
<% end %>

Rather than have this in two separate files and then run the risk of updating one and not the other with future updates, we can refactor this into a partial.  Sounds like it could be complicated, but it is way easier than it sounds once you have a couple of practice runs in.  Create a new file in the Purchase called 'form.html.rb'.  Now, copy and paste the form into this new file.  In your new and edit files, use the following: '<%= render 'form' %>'.  

How does this work, you ask?  Rails has some pretty cool stuff going on behind the scenes.  Some people call it Rails magic but really, it is just a ton of hard work someone else coded and did for us so we are left to focus on creating.  Rails has something called implicit rendering.  By putting 'render form' in the new and edit files, Rails will go and look within the same folder for a partial (denoted by the " " in the file name and then plunks the code in there for you.  It will also change the submit button depending on which page you are on.  If you are on the new page, the submit button will say "Create Purchase" and the edit page, the button will say "Update Purchase" (or the applicable name based on the model).  

Partials can save you a ton of headaches down the road!  Now that I am wrapping up the Rails module, it is time to start gearing up for JavaScript!  

