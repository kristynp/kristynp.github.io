---
layout: post
title:      "Portfolio Project #2 Sinatra MVC"
date:       2020-02-14 18:20:19 -0500
permalink:  portfolio_project_2_sinatra_mvc
---


This project was very gratifying. It felt great to put all of the pieces together for password encryption, signup and login processes,  and creating all of the views, routes, and controllers needed for multiple models. 

I started out by creating a repository on github, and then began creating my file structure to include a config ru, a rakefile, and a gemfile. 

After that I began adding in the gems that I knew I would need for the project. I'm grateful that there are such excellent gems available such as 'bcrypt' that are widely trusted and integrated with Active Record, and that there is a wealth of available knowledge on getting applications started, both available from Learn, and various online resources. 

At that point I could move on to getting my database set up, including writing migrations for tables to create the schema I wanted. Since I used associations, including users with a has_many plants relationship and plants with the relative belongs_to user relationship, the models needed to be set up so that Active Record could aid in setting up automatic association of those connections upon creation of new objects. This required my plants table having a user_id column to associate the plant with the correct user. 

I enjoyed the process of creating each of the routes with associated views. It feels intuitive to me to make a route, check to make sure that it displays text, create the view, then send a route to the view, check to make sure that the browser will show that view, write the forms or view code to show what needs to be displayed, then create a form to send information and a route to receive the information. 

I would occasionally forget to commit changes as frequently as I should, so some of my commits were larger than they probably should have been, so that is something I must improve on. 

Overall, I'm enjoying the process of creating functional web applications, and it has felt good to create something that alludes to real world functionality.
