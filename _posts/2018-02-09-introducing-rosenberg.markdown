---
layout: post
title:  "Introducing 'Rosenberg'"
date:   2018-02-09 13:49:12 +0000
categories: technical rosenberg
---
'Rosenberg' is the code name for a game design framework and engine I'm currently working onthat tries to move focus away 
from programming technical tasks, and programming game rules. The name is after board game designer Uwe Rosenberg 
(Agricola, Caverna etc.).

The main inspiration for Rosenberg is basically two-fold:
- I find most existing prototyping techniques slow and annoying
- The lack of high-level beginner systems that emphasize design of game rulesets in the abstract sense

Rosenberg attempts to do for strategy game design what RPG Maker has done for RPG creation - create a simple tool which 
entirely focuses its design on mechanical rules and handles all the technical problems itself. As such it is takes the 
form of a game engine with a custom DSL for writing game mechanics within a turn-based structure; mechanical effects are 
then updated onto the screen. Rather than defining objects and classes as programming primitives, authors work directly 
with Components, each of which has a visible manifestation on the screen, Resources, which track internal values, and 
Rules, which act on resources and components in order to mutate the game state. Components can be placed onto ‘Boards’, 
each of which takes up a section of the screen, and ‘Screens’ which can be layered on top of the other, opened and closed. 
The game designer should be thinking only on the highest level, about how components interact with the player and with 
each other.

Rosenberg’s DSL is a declarative language which borrows design elements from state management containers such as Vuex, 
Redux or Elm. Events are dispatched from the engine, and the given rules listen and, if they should trigger, relay their 
instructions to the engine, which then implements them and updates the graphical representation accordingly. The language 
is intended to be as close to data as possible; the plan is to provide a form-based editor for tweaking and creating 
parameters, with mutators provided that allow various types of generic state transformation commonly needed in games. 
Custom mutators will be possible to create for more technical users; currently these are done by compiling in custom C 
functions using a provided builder, but there is planned a Lua scripting option too for faster iteration. Plugins will be 
creatable that provide suites of custom functions to provide more sophisticated functionality that can then be shared in a 
community.

The primary usefulness of Rosenberg will probably be in rapid game prototyping, but the plan is to allow users to release 
their games as full products as well if they desire. The engine will come with a large array of pre-created tokens and 
graphics for players to use, which are easily swappable for custom art by specifying configuration.

Technically speaking this is fairly early in development. It's written in C using SDL as the graphics library. Hopefully
more as it progresses! The language itself is capable of handling most of the rules of chess correctly (with the exception
of castling and en passant, both of which require more sophisticated state management). I'm excited about this project
and hope it'll at least be useful for me in my prototyping.
