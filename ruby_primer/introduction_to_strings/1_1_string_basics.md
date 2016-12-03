# 1.1 String Basics
## String Interpolation

It is essential to be able to replace placeholders within a string with values they represent. In the programming paradigm, this is called "string interpolation". In Ruby, string interpolation is extremely easy. Feel free to run the example below to see the sample in action.

```ruby
# irb --noecho
>> a = 1
>> b = 4
>> puts "The number #{a} is less than #{b}"
The number 1 is less than 4
```

Do remember that placeholders aren't just variables. Any valid block of Ruby code you place inside `#{}` will be evaluated and inserted at that location. Isn't that very neat?

Now let us see you wield this tool. Complete the functionality of the method below which, given a String as the argument, inserts the length of that String into another String:

```ruby
def string_length_interpolater(incoming_string)
  "The string you just gave me has a length of #{incoming_string.length}"
end
```

We've been using double quotes in all our string interpolation examples. A String literal created with single quotes does not support interpolation.

The essential difference between using single or double quotes is that double quotes allow for escape sequences while single quotes do not. What you saw above is one such example. `“\n”` is interpreted as a new line and appears as a new line when rendered to the user, whereas `'\n'` displays the actual escape sequence to the user.

Let us move on...

## Search in a String
Another common scenario is checking if a String contains any given character, word or sub-string. Considering your experience with the Ruby API and its intuitiveness, try and check whether the String given below includes 'Yoda'.

```ruby
>> '[Luke:] I can’t believe it. [Yoda:] That is why you fail.'.include? 'Yoda'
=> true
```

Did you manage to figure that out by yourself? Too many cooks spoil the broth while too many hints lead the hunter astray! Now check if the string below starts with 'Ruby'.

```ruby
>> 'Ruby is a beautiful language'.start_with? "Ruby"
=> true
```

After that, checking whether the statement below ends with 'Ruby' should be easy.

```ruby
>> "I can't work with any other language but Ruby".end_with? 'Ruby'
```

Are you getting the hang of the Ruby API? The previous three methods all ended with a '?'. It is conventional in Ruby to have '?' at the end of the method if that method returns only boolean values. Though it is not mandated by the syntax, this practice is highly recommended as it increases the readability of code.

Sometimes we will be required to know the index of a particular character or a sub-string in a given String and conveniently Ruby provides a method on String that does exactly that. Try and find out the index of 'R' in the string below:

```ruby
>> 'I am a Rubyist'.index 'R'
=> 7
```

## String case change
The last thing we will look into in this lesson is manipulating the case of strings. Ruby provides us with a convenient tool-set to take care of proper and consistent casing within strings. Let's start with converting a string in lower case to upper case.

```ruby
# irb --noecho
>> puts 'i am in lowercase'.upcase #=> 'I AM IN LOWERCASE'
I AM IN LOWERCASE
```

Similarly, one can convert a string to lower case as well. Ruby calls this method downcase. Convert the string below into lower case.

```ruby
# irb --noecho
>> puts 'This is Mixed CASE'.downcase
this is mixed case
```

On a parting note, let us touch on an interesting method. When you encounter a mixed cased string, Ruby provides a way to swap the case of every character in it i.e. this method would convert "I Am MixEd" to "i aM mIXeD". Try to figure this method out and tell us if you ever come across a scenario where you find use for this. It might make a good story for a rainy night!

```ruby
# irb --noecho
>> puts 'ThiS iS A vErY ComPlEx SenTeNcE'.swapcase
tHIs Is a VeRy cOMpLeX sENtEnCe
```

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_strings/1_0_introduction_to_strings.md)
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
[\[next\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_strings/1_2_advanced_string_operations.md)
