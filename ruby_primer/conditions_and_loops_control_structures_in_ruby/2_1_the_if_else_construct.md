# 2.1 The if..else construct
## Ruby Conditional Branching : the 'if' statement
You can use Ruby's Boolean Expressions to specifiy conditions using the usual `if..else` construct. Let us take a look at a simple example:

```ruby
def check_sign(number)
  if number > 0
    "#{number} is positive"
  else
    "#{number} is negative"
  end        
end
```

When you run the above example, it will tell you that `0 is negative`. But we know that zero is neither positive nor negative. How do we fix this program so that zero is treated separately?

Ruby gives you the `elsif` keyword that helps you check for multiple possibilities inside an `if..else` construct. Try using elsif to fix the code below so that when the number is zero, it just prints `0`.

```ruby
def check_sign(number)
  if number == 0
    number
  elsif number > 0
    "#{number} is positive"
  else
    "#{number} is negative"
  end        
end        
```

Ruby also has an `unless` keyword that can be used in places where you want to check for a negative condition. `unless x` is equivalent to `if !x`. Here is an example:

```ruby
# irb --noecho
>> age = 10
>> unless age >= 18
>>    puts "Sorry, you need to be at least eighteen to drive a car. Grow up fast!"
>> end
Sorry, you need to be at least eighteen to drive a car. Grow up fast!
```

## The ternary operator
In english, "ternary" is an adjective meaning "composed of three items." In a programming language, a ternary operator is simply short-hand for an if-then-else construct.

In Ruby, `?` and `:` can be used to mean "then" and "else" respectively. Here's the first example on this page re-written using a ternary operator.

```ruby
def check_sign(number)
  number > 0 ? "#{number} is positive" : "#{number} is negative"
end
```

## Truthiness of objects in Ruby

The conditional statements `if` and `unless` can also use expressions that return an object that is not either true or false.

In such cases, the objects `false` and `nil` equates to false. Every other object like say `1`, `0`, `""` are all evaluated to be `true`. Here is a demonstration:

```ruby
>> if 0
>>   puts "Hey, 0 is considered to be a truth in Ruby" 
>> end
Hey, 0 is considered to be a truth in Ruby
```
