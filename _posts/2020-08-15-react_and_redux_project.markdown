---
layout: post
title:      "React and Redux Project"
date:       2020-08-15 13:49:40 +0000
permalink:  react_and_redux_project
---

## Inspiration and Tools to Use

E-Commerce applications are things we see in our society almost on a daily basis. When finding inspiration for my final Flatiron project I felt it was time to make a E-Commerce site of my own. React is a powerful framework, and is mostly focused on managing state. Managing state is a skill that was somewhat new to me at the start of this project, but utilizing Redux to track state made things a lot simpler. State is a lot easier to see with Redux because it is all housed in one area, and dabbling with mapping state and dispatch to props to connect React and Redux was good practice. 

## Authentication in React

I have experience with authentication in Ruby and Rails, but this was my first time creating an authentication system in React. Authentication systems all have similar pieces including sign up forms, log in verification and logout session deletion. Since the backend of this project was a Ruby on Rails API we created, this made creating an authentication system pretty straightforward. In Ruby there is a Session Hash, that you can store the id of the current user in to determine who is currently logged in. React doesn't have a Session Hash as far as I am aware, but we can use state to make the same results occur. When a user logs in it should send the data from the login form to the rails backend, which verifies the credentials and sets the session[:user_id] to the id of the user who just logged in. Rails can then find that user and send it back to React and we can store it in a Current_User piece of state in Redux. If this is done correctly a user should stay logged in until the logout functionality deletes the Session Hash data on the backend or we set some type of expiration. 

## Stores and Items CRUD and Transaction Logic
Once authentication was complete the next important task was to make Create, Read, Update, and Delete(CRUD) functionality for users to be able to create a store and add items to it. I made the decision for users to each have one store for simplicities sake, allowing users to have multiple stores is something I could add in the future if needed. Each of these CRUD actions involved actions that took data from the front end to send to the backend which adjusted the database in whatever way needed, and then sent the new data back to the front end for the reducers to update in the state. Transactions occur when a user in my application "purchases" an item from another user's store. When this occurs, a conditional on the backend is checked to determine if the buying user can afford the item, and if they can, the item is "purchased" and removed from the store while the balance of the buyer and seller will update accordingly. 

## Things Still to Add in the Future
Some stretch goals I didn't have time for in the context of this project's timeframe include adding a shopping cart for users to be able to buy multiple items at once and adding a purchased_items attribute to users that updates with the items they bought and the day they bought them. Both are managable goals that I intend to add for practice in the future. If this app were ever made more realistic, the process of adding funds would need to change to actually adding funds from people's bank accounts and the items purchased would actually need to be authenticated as real items and shipped to the buyer when bought. In the context of the project though these are aspects we can imagine how they would work in reality. All in all, I had a good experience with this project and feel a lot more comfortable with the powers lended by React and Redux.

