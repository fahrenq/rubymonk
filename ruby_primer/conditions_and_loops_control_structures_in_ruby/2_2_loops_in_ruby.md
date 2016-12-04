# 2.2 Loops in Ruby
## Loops in Ruby

Loops are programming constructs that help you repeat an action an arbitrary number of times.

The methods `Array#each`, `Array#select` etc. are the most frequently used loops since the primary use of loops is to iterate over or transform a collection, something that we'll learn in the chapter on "Arrays in Ruby."

Here we will cover two basic looping constructs you can use to solve most other looping requirements that may come up.

### Infinite Loops

Infinite loops keep running till you explicitly ask them to stop. They are syntactically the simplest to write. Here goes one:

```ruby
loop do 
  puts "this line will be executed for an infinite amount of time" 
end
```

The example above does not have a termination condition and hence will run till the process is stopped. A loop can be halted from within using the `break` command.

Now write an infinite loop where the monk will meditate till he achieves Nirvana. Use the `break` statement once Nirvana is reached.

```ruby
loop do
  monk.meditate
  break if monk.nirvana?
end
```

### Run a block of code N times

Say N is 5, let us imagine how it might look.

```ruby
5.times do
  # do the stuff that needs to be done
end
```

Well, we imagined it right. It is that simple!

Here is a task for you to test your newly learned looping skills. We have a bell outside our monastery that people can ring in times of need. Write a method that can ring the bell N times, where N is a parameter passed to the method.

```ruby
def ring(bell, n)
  n.times do
    bell.ring
  end
end
```

We've only scratched the surface of the various ways in which Ruby lets you write loops. However, this should be enough for the most common use cases. Let us know if you need more!
