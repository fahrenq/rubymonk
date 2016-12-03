# 1.0 Introduction to Strings
## String construction
In doing lies the true path, so let us begin by doing. Type out `"Ruby Monk"` in the box below (remember to include the quotes).

```ruby
>> "Ruby Monk"
=> "Ruby Monk"
```

Strings are key to communicating with a user and programming apprentices will encounter and start manipulating strings from the earliest stages of their journey. In this lesson, we will explore some of the tools Ruby provides to create and manipulate strings.

## Literal forms
String construction has what is known as a literal form - the interpreter treats anything surrounded with single quotes (`'`) or double quotes(`"`) as a string. In other words, both `'RubyMonk'` and `"RubyMonk"` will create instances of strings.

It's your turn now; go ahead and create a string that contains the name of the current month. Like, 'April', or 'December'.

```ruby
>> 'December'
=> "December"
```

Action etches deeper into the memory than mere words. Recreate the string in the exercise above using double quotes (`"`). You'll see that the tests pass the same way as they did before.

```ruby
>> "December"
=> "December"
```

The single quoted and double quoted approaches have some differences, which we will look into later. For most purposes they are equivalent.

All `Strings` are instances of the Ruby `String` class which provides a number of methods to manipulate the string. Now that you have successfully mastered creating strings let's take a look at some of the most commonly used methods.

## String Length
As a programmer, one of the common things you need to know about a `String` is its length. Instead of merely telling you how to do this, let me share a secret about the Ruby API with you: Try the obvious! The Ruby core libraries are very intuitive, and with a little practice you can effortlessly convert instructions in plain English to Ruby.

Test your intuition and try to change the code below to return the length of the string `'RubyMonk'`.

```ruby
>> 'RubyMonk'.length
=> 8
```

That shouldn't have taxed your intuition too much! Let's move on to slightly more complex concepts.

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_ruby_objects/0_2_syntactic_sugar_for_special_methods.md)
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
[\[next\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_strings/1_1_string_basics.md)
