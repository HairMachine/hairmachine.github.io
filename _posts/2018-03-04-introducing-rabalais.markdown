---
layout: post
title:  "Introducing 'Rabalais'"
date:   2018-03-04 13:49:12 +0000
categories: technical rabalais
---
Rabalais is at heart a simple DSL for specifying triggers attached to textual information, and responses to player choices 
in dialogue. It is designed to not be standalone but to work alongside other systems; a plugin for RPG Maker is already 
working, and it will obviously connect with Rosenberg in a simple fashion. Each implementation of the Rabalais language 
will interface with the provided system’s state management. It's named after a French monk who was instrumental in
the development of the French language. My naming schemas are so great right?! One thing I've noticed is it's hard to
type correctly. My fingers keep doing 'Rabalias'.

I was motivated to create Rabalais by a couple of things:
- The lack of a portable dialogue engine that isn't tied to some other huge framework, like Unity or the like
- The want for a more powerful, non-tree based system specifically designed for dynamic and reactive storytelling

Specifically I was playing around with an 'epic fantasy RPG' in RPG maker and finding the inbuilt tools hopelessly
unfit for my purposes.

The language specification is currently simple; a few operators combined into expressions to check whether a particular 
text box should trigger, reading variables and comparing them to user-provided values; if the expression evaluates as 
true, the textual payload is returned. Rabalais supports simple branching tree-structures within a single node to make 
writing simple dialogue trees bearable, has the ability to give the player a number of fixed choices (each of which can 
be made conditional on state) and can also update state variables as a result of player choices.

The structure of a Rabalais is not representable as a simple two dimensional tree, as any box can connect to any other 
depending on how the game state moves. This is powerful but also will become incredibly hard to organise; to that end an 
important part of the Rabalais project is an editor that - in addition to creating nodes and controlling on which state 
they’re active - allows the designer to simulate the game state and observe which values will be available in which specific 
situations, as well as alter these state values themselves and observe which nodes become active or inactive.

Rabalais is intended to become more complex and facilitate greater levels of sophistication, particularly in regards to 
procedural text generation based on state.
