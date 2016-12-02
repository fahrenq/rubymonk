# 0.0 Introduction to Objects
## Everything is an object
We will begin our journey with objects.

In Ruby, just like in real life, our world is filled with objects. Everything is an object - integers, characters, text, arrays - everything.

To make things happen using Ruby, one always puts oneself in the place of an object and then has conversations with other objects, telling them to do stuff.

Roleplaying as an object in your program is an integral part of object-oriented programming. To know which object you are at the moment, one may use the keyword self.

```ruby
>> self
=> main
```

As you can see, if you don't specify which object you are, you automatically play the role of the main object that Ruby provides us by default.

We'll delve into how one can play the role of different objects and why this is useful a little further down the line.

## Talking to objects
One object interacts with another by using what are called `methods`. More specifically, one object "calls or invokes the methods" of another object.

In the example below, we call the method `even?` on the object that is the number `2` by placing a period (`.`) after the object, then adding in the name of the method we want to invoke.

```ruby
>> 2.even?
=> true
```

Invoking a method on an object inevitably generates a response. This response is always another object. Calling the method `next` on the object `1` has it give us the next consecutive value, `2`.

One may also chain method invocations by simply adding more periods and method names sequentially - each method in the chain is called on the result of the previous method. Go on and try it by invoking `next` twice on `1` to get `3`.

```ruby
>> 1.next.next
=> 3
```

The results you're looking at are the consequence of running a series of tests against your input to validate it. If you see results coloured red, this means one or more tests failed. Green means you're good to go.

[next](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_ruby_objects/0_1_more_objects_and_methods.md)
