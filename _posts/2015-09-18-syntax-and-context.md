---
layout: post
title: Syntax and Context
---

Wow.  I can't believe it's been over a week since my last post.

I've been finishing up a second Web App and working on the fundamentals of Object Oriented Programming, building a class for playing cards and a class for a deck of cards and making them play well together (pun fully intended.)

Last night when I got home from playing DJ (note: I'm not a DJ, but sometimes I play one on the radio) I got back to the business of studying Ruby.  I wanted to at least read through my lesson/challenge for today so that I could let my brain crunch on it over night.  All hail unconscious cognition!

Problem was, when I was reading through one of several linked documents on Fun with Arrays I found a mildly confusing line of code using "<<" to build a puts output.  Aroo?

Learning a new programming language is much like learning any communal human language.  Not only do you have to learn the vocabulary, you have to learn the proper sentence structure, syntax and punctuation.

In programming languages that means learning lots of new operators and syntax.  Programmers prefer to be, let us say, *EFFICIENT* by nature (some may call it a tendency towards laziness,) so there are also a lot of contextual shortcuts used in programming languages. 

Reading code is very similar to reading pure Physics or pure Math: Comprised of symbolic notations and flagrant abuse of the greek alphabet, it can be intimidating to the uninitiated.  Learning to read code can sometimes be the equivalent of learning to read hieroglyphics.  If you are caught without your Rosetta Stone it can be confusing at times.

That was certainly the position I found myself in as I was reading a blog post about 2D Arrays.  In it there was sample code using a puts statement with an each_index loop to walk through array values and output them to the screen with other characters and spaces to be organized in a meaningful way for the reader.

Working with Arrays, the "<<" operator is generally used to push a value on to an array.  It was clearly NOT being used to do that in the puts statement.

After much searching and hair-pulling I found that in the context of Strings "<<" is a concatenation symbol to append a value to the current string.  Granted I could see from the code and expected output that that was the *anticipated* action of the symbol, but my journey to the supporting documentation led me a merry chase through the land of string-literals and Here Doc notation.

RTFM right?

I don't know if this was a case of me missing that left turn at Albuquerque or a case of contextual foul.  I DO know that multiple functions of the "<<" operator are now well-cemented in my brain, specifically BECAUSE it was a point of contention for me that required special attention for clarification.

I'm considering this detour as I would consider taking the scenic, tree-lined, hilly route on my Mean Streak... I'm out to enjoy the ride. 

~AMP