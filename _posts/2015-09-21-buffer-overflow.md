---
layout: post
title: Buffer Overflow
---

<img src="https://s-media-cache-ak0.pinimg.com/474x/cc/1d/10/cc1d10f10629131cbe16645cfd2a240f.jpg">

Life has been disrupting my study time a lot in the last week.  I finally got some uninterrupted time to power through a lot of lessons and assignments to get caught up yesterday.  About 8 hours in I was feeling a lot like that classic Far Side above.

With the intensity of some of my study sessions I worry about retention.  I promise myself I'll go back and run through all these basics again to reinforce what I'm learning.  Time constraints may make that a difficult proposition.  But at least I am reinforcing what I learn as I encounter different concepts in different contexts and can thus build complex interconnections of neural pathways.

In programming for a computer, simple and elegant are ideal.  Make things work in the least complex fashion and eliminate potential points of failure through conscious design and careful implementation.

In programming a human brain the more ways you can find to build pointers to new knowledge the better it will stick.  Perhaps that's why I write mental methods to describe processes I encounter in the  world.  And revisit them when I learn more about Ruby, refining and refactoring.

{% highlight ruby %}
puts "Number of wags?"
wags = gets.chomp.to_i

def tailwags(wags)
	side = "right"
	wags.times do
	    puts side
    	if side  == "right"
    		side = "left"
    	elsif side == "left"
    		side = "right"
    	end
    end
end

tailwags(wags)
{% endhighlight %}

I was watching water boil the other day, trying to picture the code I would write to describe the transformation of thermal to exothermic to kinetic energy that happens when water boils.  I don't have that one yet, perhaps in the future.

Hmm... now I'm relating this back to OOP and trying to decide if I should define a Class for Boil and define Methods for types of energy transformations and for the chemical process of breaking apart the H<sub>2</sub>O molecule within that Class.

There we have it.  Interconnections.  Reinforcing each bit of new knowledge I gain about Ruby by connecting it back to other knowledge that is already in my brain.  Sometime this takes me off on tangents.  (Like when I use the word 'tangents' and then flash on writing a method to compute tangents to a circle, and a Method to circumnavigate a circle within a Class for Circle... which takes me back to my Logo days and "down turtle" as I program the computer to draw a circle.)

<p class="message">
This trippy programming-of-yore flashback has been brought to you by the letter: <span style="Font-size: 24px">ə</span>
</p>

See?  Buffer Overflow.  Perhaps it's time for a reboot.  :-)

And now back to our regularly scheduled programming.

~AMP