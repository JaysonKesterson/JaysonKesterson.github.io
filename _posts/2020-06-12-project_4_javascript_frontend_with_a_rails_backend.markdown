---
layout: post
title:      "Project #4 : Javascript Frontend with a Rails Backend"
date:       2020-06-12 17:07:51 +0000
permalink:  project_4_javascript_frontend_with_a_rails_backend
---



Call me a nerd if you want, but growing up I spent countless hours on quiz websites with friends and going to trivia nights at local restaraunts. This led me to always wanting to create my own trivia quiz website, and this project provided an opportunity to get started on it. Javascript provided a nice base of tools for creating the front end the way I had it sketched out in my head, but the fact that this was the first project we have used an extensive amount of Javascript made it a little intimidating. I've also always been really into Statistics, being my minor in college, whether it was through sports or just any type of data that can explain different phenomena about the world. Therefore the concept of creating my own API to use as the backend of the project was exciting too, and being comfortable with Ruby on Rails meant that the backend process didn't pose much of a problem.

## Utilizing Fetch is the Key

Fetch. Fetch. Fetch. Fetch() basically allows you to make network requests to link the frontend to the backend. This is essentially how the frontend receives the JSON data from the backend and then allows you the ability to manipulate this data on the frontend to display it to the viewers. Using fetch to get data from the backend didn't have too many obstacles, I mostly used the GET functionality of fetch to grab the data from the API and use it to make new instances OOJS objects in order to display and organize data. Posting with fetch() is a little more complicated, and this is where you can send data from the frontend to update your backend database using fetch. I ended up running into an issue when I was trying to create an instance of the Quiz model at the same time as all of its associated questions. I originally tried to do this by calling a function I had created called postQuestion() that was posting to the create action of my Questions controller inside of an iteration that was being ran once for each question trying to be created. Long story short, the server didn't like that. I eventually decided to send all of the questions as an array to my Quizzes controller since Quizzes and Questions are related with a has_many relationship and utilize .build to create all of the questions there. Running into walls and then learning how to jump over them is a great learning experience, and I feel a lot more comfortable with fetch than I did before this project.


## Functionality of the Quizzes

Creating the ability for a quiz to be played was the most enjoyable part of this project. This process started by adding eventListeners to buttons next to each quiz, which would render the quiz questions next to input boxes for the answers and a submit button. The next step was adding an eventListener to the form, which then would compare each user inputted answer to the correct answer of the question and keeping a tally of how many they got right and wrong. Finally, a results page is loaded which tells the user how many they got right and the exact questions they got wrong, allowing them to go back to the home page at any time to play a different quiz or create a new one. No refreshing needed at all!

## Features to Add

If I continue to develop this application there are a plethora of features I would love to add. As of now, I only have three categories of quiz being sports, music and random knowledge. This could definitely be expanded to a wide variety of options, I just left it as these three for the sake of the project. I also would like to implement a timer for each quiz, and once that timer reaches zero it would automatically submit the quiz to create a sense of tension in the user being pressed for time. Finally I would want to add user authentication and some type of stat system for users. Maybe they would be able to see their average score on sports quizzes, their highest score on a music quiz, or the amount of quizzes they have taken total.
