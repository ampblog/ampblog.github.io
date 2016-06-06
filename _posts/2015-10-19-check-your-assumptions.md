---
layout: post
title: Check Your Assumptions
---

I spent much of the weekend frustrated. The REASON I was frustrated was because I didn't Check My Assumptions.

I was working on a coding challenge.  My solution involved having two copies of a multi-dimensional Array.  I would inspect the first copy (hereafter FC) and based on the results of the inspection make CHANGES to the second copy (SC). This wasn't necessarily a difficult proposition.  I had already solved this problem once and was working on a refactor to improve efficiency.

I started with a clone of my original code and I set about making modifications to eliminate a secondary method and fold it in to the initial iteration of the Array.

Every time I ran the refactored code I found that it was not only changing the SC of the Array, but also the FC. <em>Note: Needed deep copy by way of Marshaling, 'tis another story.<sup>1</sup></em>

The thing that was frustrating the begeebers out of me was that each time I reran my original solution IT WORKED!  The FC was unchanged and the SC was properly modified HUZZAH!

...Except that that WASN'T actually the case.

I needed to <span><u>Check My Assumptions</u></span>.

I forgot that I had changed the order of the methods I called when I tested my refactored script. And while the original solution DID properly make changes to the SC, it WAS simultaneously changing the FC. Problem was I didn't know that because I was only inspecting the FC BEFORE calling the method to apply the changes to the SC.

I hadn't held my test methodology constant in the refactored script, so I was seeing a different set of results. Once I realized my error I changed the order I was calling the methods in my original solution script and found that IT TOO had changed the FC at the same time it was changing the SC.

Had I just Checked My Assumptions I might have saved myself days of frustration and headaches as I chanted over and over "But it worked in the original solution!"

## Check Your Assumptions At The Door!

The moral to this story is this: Check Your Assumptions. Start with a fresh pair of eyes EACH AND EVERY TIME you look at the code. Reset your expectations. Go back and examine your code, your methodology, your order of invocation. Faulty assumptions are PEBKAC 100% of the time, so CYA.

~AMP

<small>1. [Marshal](http://ruby-doc.org/core-2.2.2/Marshal.html), and [a lovely way to invoke Marshaling to achieve Deep Copy](http://stackoverflow.com/a/1465787#1465787)</small>