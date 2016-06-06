---
layout: post
title: A Number Stack
date: 2015-10-23
---

So I wrote a Stack Class in the process of working on a new coding challenge yesterday. The Stack was explained as an abstract data structure that is Last-In-First-Out. I needed to have a functional stack to complete my assignment and at some point I went off on a tangent to code a Number Stack.

This is somewhat my ode to the IP Stack, in that it encodes data and bit lengths to represent items on the Stack.

{% highlight ruby %}
class NumberStack
	attr_reader :data, :topval

	def initialize
		@data = nil
	end

	def push(value)
		value = value.to_s(16)
		@data = "#{value.length.to_s(16)}#{value}#{@data}"
	end

	def pop
		length = @data.byteslice(0).to_i(16)
		topval = @data.byteslice(1, length).to_i(16)
		remainder = (@data.length - length)
		@data = @data.byteslice((length+1), remainder)
		topval
	end
end
{% endhighlight %}

[Or Find Gist here](https://gist.github.com/amarkpark/ee48eeaf7803d200b085.js)

There is a functional limit to the integers that can be pushed to the stack of 1152921504606846975.

That is "fffffffffffffff" in Hexadecimal.

I could increase the functional limit by changing the base I convert to to push the data onto the stack, but I didn't need a gianormous limit and I'm used to working with Hex so I kept it simple.

~AMP