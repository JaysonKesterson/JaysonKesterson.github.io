---
layout: post
title:      "Rails Portfolio Project"
date:       2020-04-16 18:57:39 +0000
permalink:  rails_portfolio_project
---

## Getting Started

Models and their associations. The first hurdle in this project was 100% deciding on a group of models that associate to each other in a manner that makes realistic sense, and also meets the requirements of the project. After hours of deliberating what group of models I wanted to use for my project and how I wanted them to associate, I settled upon the Many to Many relationship, "Fans have many Teams" and "Teams have many fans". The next question was what model would make sense as the join model for these models. I tried sport and players, but neither seemed to make much realistic sense when writing out how all of the models would relate. I was suggested to use a FanTeam model, which ended up making by far the most sense relationship-wise so I committed to it and it led me to a lot of success in creating features I had visualized adding to my application.

## Adding Features
Omniauth is probably one of my favorite additions to add to my knowledge of programming. Not only is it much easier than I anticipated it being, being able to link my applications to log in with Facebook or other well-known programs definitely makes me feel more integrated as a developer. Almost every application I have come across recently gives users the ability to log in from third party sources, and before omniauth I hadn't a clue how that was being done on the back end. Adding these third party log ins is a huge feature in my eyes and I am glad to now know how to implement it via the Omniauth gem.

One of the features I most wanted to add was to nest players inside of teams and give fans the ability to add players to teams, which after reviewing nested resources from previous labs was pretty simple. The issue I have come across is whether I want to allow fans to delete/edit these teams, since the team's players arent directly related to the fan, just the team. If I allow them to edit/delete they could affect players added by other fans, which could be an issue. One solution I have been toying with is the idea of only allowing admins to edit/delete, whereas fans can add them. At the time of writing this blog I still haven't entirely decided the best way to handle that. 

One of the more interesting things I incorporated was the attribute ':die_hard_fan' on the FanTeam model to meet the requirement of having a user submittable attribute on the join model. I decided to nest this attribute on the form for when a fan creates a team to meet the nested form requirement. Fans can select whether they are a die hard fan of that team or not on the new team form this way. The fan's profile has a separate list for the teams they are a die hard fan of and on the home page the current fan's die hard teams will be highlighted green amongst the other teams created by different fans.

## The Takeaways

Strictly comparing Rails to Sinatra as a framework, it is no debate that Rails has a LOT more to offer from the perspective of a developer. Having so many more tools in the figurative toolbox gives a developer many more options to fix issues and add features to an application, but sometimes finding the right tool can be more difficult when you have so many tools available. Tinkering with this application has shown me that with the help of a browser and the rails documentation anything can be done with a little research, and I am confident in my ability to be able to figure out how to implement features from the documentation more now than I was before this project.
