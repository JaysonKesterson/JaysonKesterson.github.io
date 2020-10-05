---
layout: post
title:      "Data Structures: Queues vs. Stacks"
date:       2020-10-05 13:52:19 +0000
permalink:  data_structures_queues_vs_stacks
---


Understanding Data Structures is helpful in all areas of programming, and they show up time and time again in tech interviews. Learning Software Development from Flatiron School's Software Engineering program taught me a lot of concepts, but Data Structures weren't a main focus. Initially when reading documentation on Data Structures I would ask myself, why can't we just use an Array or an Object for this? I eventually realized that some of these structures can easily be represented by Arrays in its most basic form, but you'd need to inspect further in order to fully understand it’s potential. A Data Structure is not just the way your data is structured, but also the logic associated with it. The way data is inserted, what happens to itwhile inside the structure, and even the way it can be removed. This is where the real utility of data structures is, and their actual purpose.

## Queues
Queues are best utilized in a situation where you need to handle a list of items that need to be executed in the order they were created. Queues are described to use the FIFO approach (First in First Out). This is best described in a real life scenario where a person is waiting in a line at the store, the first person who joined the queue will be the first person served. Queues are usually Arrays as the basic data structure, but follow the rules of a queue mentioned above. To implement queues, the most important methods to know are enqueue and dequeue. Enqueue add elements to the queue whereas dequeue removes them. Types of queues you may come across are priority queues, circular queues and double ended queues. Priority queues are sorted by a priority value, circular queues have the last element pointing to the first element (creating a circle effect), and double ended queues allow items to be removed from the beginning and end of the queue.

## Stacks

Stacks are a data structure that unlike queues, use the First In Last Out flow. Imagine a stack of books on a table, if you add a book to the top of the stack and then decide to grab a book later on, you will grab the book from the top of the stack. Therefore the first book added (the one on the bottom of the stack) would be the very last one to be removed. One interesting case of a stack is one we’ve used numerous times without even knowing it: undo.  If you are attempting to undo an action, you are either trying to undo your most recent action or you are attempting to undo several actions to erase one that happened some time ago. Either way, you'd be removing elements from a stack of actions. Stacks are also often used for reversing the order of a list, since you'd be able to iterate over your list elements from first to last and store each one into a stack, then by popping them off the last one out will the original list’s first element.

## Compare and Contrast

Queues and Stacks are Data Structures that often get confused with one another due to their similarities, but their differences in fact make them opposite. The analogies of a line in a store and a stack of books above hopefully made it clear the ways that queues and stacks operate differently. The main thing to remember is the flow of the data, whether it be FIFO (First in First Out) with queues, or FILO (First in Last Out) with stacks. Another way to notice the difference here is that removing data in a queue is like using the shift method, which removes and returns the first item in a collection, whereas removing data in a stack is like utilizing the pop method which removes and returns the last item in a collection. These concepts might come up in interview questions or in your day to day coding lives, so make sure to understand the differences.
