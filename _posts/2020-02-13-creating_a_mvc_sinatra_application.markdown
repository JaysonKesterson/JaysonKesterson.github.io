---
layout: post
title:      "Creating a MVC Sinatra Application"
date:       2020-02-13 18:11:18 +0000
permalink:  creating_a_mvc_sinatra_application
---

## **Project Objectives**

The objective of this project is to create a simple Sinatra application while using the Sinatra framework along with SQLite3 and ActiveRecord. The requirements state that there should be two or more models, one being a User model that has sign up, log in, and log out functionality. The log in attributes need to be unique to a user and the user input should have input validations. The User model should have the "has many" association with another model that "belongs to" the user. Users should be able to perform basic CRUD (create, read, update, delete) functionality on the objects that belong to them, ensuring they can't update or delete objects that belong to other users.

## **Getting Started**

The first challenge to overcome in any project that involves any level of creativity is getting started. For me, I was overflowing with ideas including bucket lists, travel destination checklists and cook books. I eventually decided on using goals as a model that belongs to the User model because I felt it was the most versatile and motivational for users that may use the application. The second obstacle to overcome when creating a new application is structuring the files and dependencies. Luckily, I was told about a helpful gem called Corneal. This gem sets up the file structure for a Sinatra application for you, which is extremely convenient, but I really recommend studying the structure of the application to really ensure that you understand it. I also recommend structuring your database and creating the tables that you will need to save data for the rest of your project.

## **Creating Functionality**

Once you've decided on your models and their associations, I believe it is most practical to start from the User model. Use the attributes that your database is looking for for users to sign up and log in with and ensure you use ActiveRecord validations to ensure your database won't be persisted with bad data. From the application controller, code out some helper methods to help you along the way, enable sessions and code out the routes for your index page. 

Create a user controller and code out the sign up, log in and log out routes utilizing forms you create in your views. Don't forget the params hash and sessions hash! Remember that in applications like these, there are things users should only be able to see when signed in, and should have different options when they are not currently signed in.

Your "belongs to" objects need a controller for themselves too, to separate concerns. This is where you can create the CRUD functionality portion of your project. Users need to be able to create, read, update and delete their objects. Utilize forms and the middleware given to us by "Rack::MethodOverride" which you should include in your config.ru file. Keep in mind where you want your users redirected to when creating this functionality. Do you want them redirected to their profile page after deleting an object? Maybe you want them redirected to a specific objects show page after editing it?

## **Test, Test, and Test Again**
Once you feel your application is working properly, it is time to begin the testing phase. Determine all of the things that could make your application break and attempt to break it in as many ways possible as you can. I can gurantee you that you will find something that you didn't expect. As a programmer we envision our users interacting with our application in ways that we deem appropriate, but we need to be sure to protect our application from bad user input and anything that we don't wan't occuring in our application. Read over the requirements and test to make sure that you have them all met. Have a friend or peer interact with your application, they may discover a bug or error that you never even noticed.

## **Add features to improve user experience**
After your application has been tested in the most exotic ways you can think of, it is time to start thinking about building off of the simplicity of the application. The structure is there and funcitonal, so you can think of ways to build on top of it. Put yourself in the shoes of the user and ask yourself what you would want to see from this application. Use CSS to style your pages to make them visually appealing, maybe add a tool bar to make the user's navigation simple, smooth and seamless. After any new features are added, go back to the testing phase again to ensure it is working as you intend it to. When any new features you wanted to add are added, it meets the requirements and has been tested throughly, it is time to submit it and have it assessed by others. Be proud of yourself and confident in the work you put forward, and if any unexpected issues stem from the project, break down the errors you run into and improve your application in the future. 
