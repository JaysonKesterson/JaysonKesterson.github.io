---
layout: post
title:      "Object Oriented Ruby CLI Application Project"
date:       2019-12-06 00:18:47 +0000
permalink:  object_oriented_ruby_cli_application_project
---


After two months of learning Flatiron's Software Engineering curriculum I was feeling pretty comfortable with Ruby as a language and the relationships and concepts involving Obect Oriented Ruby. The first real obstacle for this project was working with an API for the first time, and finding one that would create a spark of creativity to write a CLI application that met all of the requirements. I stumbled across a Pokemon API and I instantly recalled how popular Pokemon Go was in the recent years as an IOS application, and my project idea became to create a rudimentaty version of that game using the Pokemon API and Object Oriented Ruby. Experimenting with the API I quickly realized that this API returned Pokemon ruby objects instead of the traditional JSON. After speaking with my Cohort Lead, she gave me the go to use this API even though it wasn't a traditional one, as long as my project met all of the requirements. 

Using bundler I generated all of the files that would be necessary for my code, including being the environment file which would set up the environment for my code by requiring necessary files and gems, executable file which would run the code, and the various class files that I would need to create to bring my Pokemon CLI to life. The first of these class files I needed to make was a CLI class. This class would encapsulate the logic that my code needed to run, and call upon other classes that I would create including a Trainer class and a Pokemon class. An instance of Trainer class would be initialized upon the startup of the application with the name that the user inputs, as the user is the trainer in this application. This trainer class instance is also initialized with an empty array "pokemon_owned", both of which having an attr_accessor creating these as attributes of the instance of the Trainer class. The Pokemon class would be initialized with a name, ability, type and trainer during the process of the CLI class, using the ruby objects given by the API. This creates the relationship between the classes Trainer and Pokemon, where every Pokemon has a Trainer, and a Trainer has many Pokemon. These Pokemon objects are randomized to be any possibility of existing Pokemon though the API to be caught by the user using an instance method catch_pokemon in the Trainer class. 

During the process of the application, users would be prompted to catch six Pokemon, all of which are shoveled onto their Trainer instance's array, pokemon_owned. After the six Pokemon are caught, a numbered list of the Pokemon owned will be displayed to the user giving them the option to learn more about each of the Pokemon in the list. If the user decides to learn more about a specific Pokemon they have captured, they will be displayed the Pokemon's species name, type, ability and trainer. Users also have the option to type 'list' which would display them the list of Pokemon they owned again to choose one to learn more about. Once the trainer is done learning about these six Pokemon, they can type exit to close the application and a goodbye message is displayed. This application can be played numerous times by typing bin/execute in the terminal, and since the Pokemon they catch are randomized they likely will catch and learn about different Pokemon each time it is played. 

This project had its challenges including learning to access an API for the first time and learning to control the flow of an application that is dependent on user input. Each user input had to be checked to ensure they are typing valid input, and if the input that is received is not an option they are prompted to give, they would need to be prompted to type a valid option. Controlling the flow through case statements and conditionals taught me to keep my code organized, so any error I come across can be deciphered and dealt with without much trouble. Altogether working on this project I learned that through programming, ideas can be brought to life with some effort, and that API's are an extremely effective way to access data to use in personal applications.








