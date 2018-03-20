---
layout: post
title:  "The conflation of design and development"
date:   2018-02-05 13:49:12 +0000
categories: philosophy
---
I think one thing holding back video game design is something inherent to its ontology. This is the fact that design
and development are often conflated, both in tooling and in how work is approached. The reason for this is pretty simple. 
In order to make a video game, you must have programmer. Video games run on computers, and the computers need to be 
instructed by writing code. This has a corollary: in order to be a solo game developer you must be a programmer.

This leads to problems immediately. Not all artists are programmers; many great video game designers may simply never 
be able to express their ideas due to a lack of technical knowledge or ability. To solve this, there are engines which 
try to reduce the burden of programming. The most successful of these at reducing the burden go hand in hand with 
aggressively restricted mechanical control for the user - they restrict far too much. Examples of these are RPG Maker 
and Adventure Game Studio. More general game development frameworks designed for beginners, such as Game Maker, provide 
paradigms that simplify development by strongly pushing mechanical expression into physically simulated interactions 
between objects - collisions, forces, movement - and reflex-based gameplay.

Ultimately, game design should be seen as a formal discipline requiring logical and mathematical reasoning as well as 
artistic intent, so any prospective designer will need to be able to think in these terms. No system currently encourages 
this or provides good tooling to develop these skills.

Worse than this, in my opinion, is the conflation of design and development. This is the casting of all game design 
problems as technical challenges; changes to rulesets are often seen as being on the same level as programming a UI, building 
map systems, dialogue systems, and other non-rule subsystems. Game programmers thus spend a disproportionate amount 
of time on technical challenges. Unfortunately, it is far easier to solve technical challenges when you know exactly what 
you are doing, so tried and true mechanics and approaches are guaranteed to be more popular. Making mechanical changes, 
unless the code has been specifically designed to be prototyping friendly, can become entangled with technical or even 
architectural changes that discourage experimentation lest the project spontaneously collapse under its own entropy. 
This is an experience all too common to the budding amateur game designer.

I believe design questions should be seen as primarily artistic questions, not primarily technical questions, and should 
be isolated from each other as much as possible. Changing game rules should not require changing game architecture, and 
vice versa.

