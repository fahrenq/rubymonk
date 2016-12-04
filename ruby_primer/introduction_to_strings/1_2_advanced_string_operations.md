# 1.2 Advanced String Operations
## Splitting Strings
In this lesson, we will have a look at some vital methods that the `String` object provides for string manipulation.

Splitting strings on a particular word, escape character or white space to get an array of sub-strings, is an oft-used technique. The method the Ruby `String` API provides for this is String#split. Let us begin by splitting the string below on space ' ' to get a collection of words in the string.

```ruby
>> 'Fear is the path to the dark side'.split ' '
=> ["Fear", "is", "the", "path", "to", "the", "dark", "side"]
```

One can effectively manipulate strings by combining String#split and a Regular Expressions. We will take look at Regular expressions, their form and usage further down the lesson.

It is possible to similarly split strings on new lines, and parse large amounts of data that is in the form of CSV.

## Concatenating Strings
You can create a new string by adding two strings together in Ruby, just like most other languages.

```ruby
>> 'Ruby' + 'Monk'
=> "RubyMonk"
```

Ruby often provides more than one way to do the same thing. The literal and expressive method for String concatenation is String#concat.

```ruby
>> 'Ruby'.concat('Monk')
=> "RubyMonk"
```

Let's try a more widely used alias. You can use '<<' just like '+', but in this case the String object 'Monk' will be appended to the object represented by 'Ruby' itself. In the first case of using '+', the original string is not modified, as a third string 'RubyMonk' is created. This can make a huge difference in your memory utilization, if you are doing really large scale string manipulations. Change the code above to use '<<' and see all the tests passing again.

## Replacing a substring
The Ruby String API provides strong support for searching and replacing within strings. We can search for sub-strings or use Regex. Let us first try our hands at something simple. This is how we would replace 'I' with 'We' in a given string:

```ruby
>> 'I should look into your problem when I get time'.sub('I','We')
=> "We should look into your problem when I get time"
```

The method above only replaced the first occurrence of the term we were looking for. In order to replace all occurrences we can use a method called `gsub` which has a global scope.

```ruby
>> 'I should look into your problem when I get time'.gsub('I','We')
=> "We should look into your problem when We get time"
```

If you haven't come across the term Regular Expression before, now is the time for introductions. Regular Expressions or RegExs are a concise and flexible means for "matching" particular characters, words, or patterns of characters. In Ruby you specify a RegEx by putting it between a pair of forward slashes ('/'). Now let's look at an example that replaces all the vowels with the number 1:

```ruby
>> 'RubyMonk'.gsub(/[aeiou]/,'1')
=> "R1byM1nk"
```

Could you replace all the characters in capital case with number '0' in the following problem?

```ruby
>> 'RubyMonk Is Pretty Brilliant'.gsub(/[A-Z]/, '0')
=> "0uby0onk 0s 0retty 0rilliant"
```

## Find a substring using RegEx

We covered the art of finding the position of a substring in a previous lesson, but how do we handle those cases where we don't know exactly what we are looking for? That's where Regular Expressions come in handy. The String#match method converts a pattern to a Regexp (if it isn‘t already one), and then invokes its match method on the target String object. Here is how you find the characters from a String which are next to a whitespace:

```ruby
>> 'RubyMonk Is Pretty Brilliant'.match(/ ./)
=> #<MatchData " I">
```

As you can see in the output, the method just returns the first match rather than all the matches. In order to find further matches, we can pass a second argument to the match method. When the second parameter is present, it specifies the position in the string to begin the search. Let's find the second character in the string `'RubyMonk Is Pretty Brilliant'` preceded by a space, which should be `'P'`.

All the complex use cases of this method involve more advanced Regular Expressions, which are outside the context of this lesson. However, on an ending note, if you ever choose to implement a parser, String#match might turn out to be a very good friend!

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_strings/1_1_string_basics.md)
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
[\[next\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/conditions_and_loops_control_structures_in_ruby/2_0_boolean_expressions_in_ruby.md)
