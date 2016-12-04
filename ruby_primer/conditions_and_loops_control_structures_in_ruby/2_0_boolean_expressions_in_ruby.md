# 2.0 Boolean Expressions in Ruby
## Beginner's Guide to Expressions in Ruby
Ruby uses the `==` operator for comparing two objects.

Let us try a simple exercise: write an expression that checks whether the value of the variable `name` is `"Bob"`:

```ruby
>> name == 'Bob'
=> true
```

The other usual operators like greater than (`>`), less than (`<`), greater than or equal to (`>=`) etc. are supported. The next exercise is to write an expression that validates whether `age` is less than or equal to `35`.

```ruby
>> age <= 35
=> false
```

Boolean expressions like the above always return either the `true` or `false` objects.

### Combining Expressions using the `&&` and `||` operators
You can use the keywords `||` (read as 'or'), `&&` (read as 'and') to combine expressions. Try modifying the following expression to check whether `age` is greater than or equal to `23` and the name is either `Bob` or `Jill`.

from:
```ruby
age >= 23 && name == 'Bob'
```
to:
```ruby
age >= 23 && (name == 'Bob' || name == 'Jill')
```

Just like the order of operations in mathematical expressions (PEMDAS anybody?), Ruby also has a set of laws governing the precedence of its various operators. However it is not something you need to be concerned about for now. Just make sure to use parentheses generously so that the order of operation is unambiguous to Ruby as well as for someone reading your code.

### Negating expressions
Ruby lets you negate expressions using the `!` operator (read as 'not'). For instance, `!(name == 'Jill')` will return false if the name is `Jill` and `true` for any other name.

```ruby
>> !(name == 'Bob')
=> false
```

Awesome! Now that you've learned the basics of writing boolean expressions in Ruby, let us see how we can use them to decide the flow of our application in the next lesson.

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_strings/1_2_advanced_string_operations.md)
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
[\[next\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/conditions_and_loops_control_structures_in_ruby/2_1_the_if_else_construct.md)
