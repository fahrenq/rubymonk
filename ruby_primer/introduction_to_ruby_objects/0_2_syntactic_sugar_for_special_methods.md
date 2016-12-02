# 0.2 Syntactic Sugar for Special Methods
## Special Methods
As an observant initiate, you've probably noticed that in the last lesson, Integer objects list mathematical operators like `+` and `-` among their methods. You probably also thought to yourself that invoking the `+` method like so - `1.+(2)` - to add two numbers would be... clumsy.

It is, though it works just fine - try for yourself by adding `4` to `3` in the exercise below.

```ruby
>> 4.+(3)
=> 7
```

Ruby as a language aims to be extremely programmer-friendly, so you can usually safely assume that there is a better way. Ruby makes an exception in its syntactic rules for commonly used operators so you don't have to use periods to invoke them on objects.

Let us rephrase the previous example in a more natural syntax by omitting the periods and brackets.

```ruby
>> 1+2   # this is same as 1.+(2)
=> 3
```

There are several other method names that have this special status - here's a quick summary of the ones you're most likely to run into.

`+`   `-`   `*`   `/`   `=`  `==`   `!=`    `>`   `<`   `>=`    `<=`    `[]`

This last method (`[]`) you've probably already seen in the lesson that covers Arrays, and is arguably the most unique in its syntax. Not only does it not require a period, it also encloses the arguments to itself. Here's a quick example to refresh your memory:

```ruby
>> words = ["foo", "bar", "baz"]
=> ["foo", "bar", "baz"]
>> words[1]
=> "bar"
```

Even more interesting is that it still works if you use the more traditional method syntax - see for yourself by running the example below.

```ruby
>> words = ["foo", "bar", "baz"]
=> ["foo", "bar", "baz"]
>> words.[](1)
=> "bar"
```

This is a common pattern in Ruby - two different ways to do the same thing where one remains consistent and the other changes the syntax to be more programmer friendly.

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_ruby_objects/0_1_more_objects_and_methods.md)
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
