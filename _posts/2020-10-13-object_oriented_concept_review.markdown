---
layout: post
title:      "Object Oriented Concept Review"
date:       2020-10-13 17:16:39 +0000
permalink:  object_oriented_concept_review
---


Some of the most important concepts to have a strong grasp on for technical interviews and programming as a whole have to do with Object-Oriented Programming. Object-Oriented programming is loosely defined as a methodology or paradigm to design a program using Classes and Objects. An object is essentially just a real world entity that has properties like a first name or a height for example, and also functionality (methods) like walk() or talk() that can be chained onto the object. An object is also an instance of a class. A class is essentially a blueprint that an object follows, so essentially a student class could have many student objects. Another imortant thing to note about Object Oriented Programming is that unlike Procedural Programming, it uses a bottom up approach. This means that we solve small problems and integrate them as a whole to find a solution, and incur a lot less redundancy than in Procedural Programming.

## Encapsulation vs. Abstraction

Two important concepts to understand regarding Object Oriented Programming are Encapsulation and Abstraction. Encapsulation is binding or wrapping code and data together into a single unit. The best example of this is a class, which has data and functionality all encapsulated in one space to act as a blueprint for objects to be created. This also involves having variables become private inside of the scope of a class, ensuring that only the class has access to them unless they are accessed through public getters and setters. Abstraction is hiding internal details and showing functionality only. An example of this would be an ATM, where you don't know the backend functionalities or languages uses, you just follow the GUI instructions to use it. If outside code wants to access the functionality of an abstraction it can be done through public functions.

## Inheritance

Inheritance is a key concept to Object Oriented Programming that involves one class passing properties to another class. In this case, the class that is passing their properties down is called the parent and the receiver of the properties is known as the child. An example of when to utilize inheritance can be seen in the example of a cat and dog class. A dog and cat would both have very similar functionality like eating, and have properties like color and size. This is because they are both animals, so to solve this issue of redundancy we can define an animal class that has the properties and functionality that all animals have, and then utilize the extends keyword to pass these traits down to the more specific dog and cat class. This example is hierarchical inheritance due to the fact that there are more than one child of the parent class. If it were just animal and dog for example, that would be single-level inheritance, and multi-level inheritance would be a situation where a parent class passes properties to a child class, but that child class is also acting as a parent by passing down its properties to another child class.

## Polymorphism

Broken down to its core, polymorphism is essentially the act of performing the same task in different ways, or the ability of an entity to take several forms. This can be broken down into static polymorphism and dynamic polymorphism. An example of static polymorphism would be method overloading because it is resolved during compile time. Method overloading is essentially the idea of having two methods with the same name, but different parameter lists. An example of dynamic polymorphism would be method overriding because it is resolved at runtime. Method overriding is mostly seen in the case of a parent class passing a method down to its child class, but that child class can override this method by writing a method with the same name and parameter list.



