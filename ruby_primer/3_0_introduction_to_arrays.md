# 3.0 Introduction to Arrays
## Empty arrays
It is easier than you think.
There is a `[]` typed into the code editor already. This is how you create an array.

```ruby
>> []
=> []
```

You can also do the same thing by `Array.new`.

```ruby
>> Array.new
=> []
```

## Building arrays
You can create an array with a set of values by simply placing them inside `[]` like this: `[1, 2, 3]`. Try this out by creating an array with the numbers 1 through 5, inclusive.

```ruby
>> [1, 2, 3, 4, 5]
=> [1, 2, 3, 4, 5]
```

Arrays in Ruby allow you to store any kind of objects in any combination with no restrictions on type. Thus, the literal array `[1, 'one', 2, 'two']` mixes `Integers` and `Strings` and is perfectly valid.

## Looking up data in Arrays
Looking up values within an array is easily done using an index. Like most languages, arrays in Ruby have indexes starting from 0. The example below demonstrates how to look up the third value in an array.

```ruby
>> [1, 2, 3, 4, 5][2]
=> 3
```
Now it's your turn - extract the 5th value from the array below. Remember that the nth value in an array has an index of n-1.

```ruby
>> [1, 2, 3, 4, 5, 6, 7][4]
=> 5
```

Array indexes can also start from the end of the array, rather than the beginning! In Ruby, this is achieved by using negative numbers. This is called reverse index lookup. In this case, the values of the index start at -1 and become smaller. The example below returns the first value in the array.

```ruby
>> [1, 2, 3, 4, 5][-5]
=> 1
```

Go ahead on try it out - extract the last value from the array below.

```ruby
>> [1, 2, 3, 4, 5][-1]
=> 5
```

## Growing arrays
In Ruby, the size of an array is not fixed. Also, any object of any type can be added to an array, not just numbers. How about appending the String `"woot"` to an array? Try using `<<` - that's the 'append' function - to add it to the array below.

```ruby
>> [1, 2, 3, 4, 5] << 'woot'
=> [1, 2, 3, 4, 5, "woot"]
```

Unlike many other languages, you will always find multiple ways to perform the same action in Ruby. To append a new element to a given array, you can also use `push` method on an array. Add the string `"woot"` to given array by calling `push`.

```ruby
>> [1, 2, 3, 4, 5].push("woot")
=> [1, 2, 3, 4, 5, "woot"]
```

Using '<<' is the most common method to add an element to an Array. There are other ways as well, but we will touch upon them later.
