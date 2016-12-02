# 0.1 More Objects and Methods
## Looking up methods
Ruby objects are happy to tell you what methods they provide. You simply call the `methods` method on them.

```ruby
>> 1.methods
=> [:%, :&, :*, :+, :-, :/, :<, :>, :^, :|, :~, :-@, :**, :<=>, :<<, :>>, :<=, :>=, :==, :===, :[], :inspect, :size, :succ, :to_s, :to_f, :div, :divmod, :fdiv, :modulo, :abs, :magnitude, :zero?, :odd?, :even?, :bit_length, :to_int, :to_i, :next, :upto, :chr, :ord, :integer?, :floor, :ceil, :round, :truncate, :downto, :times, :pred, :to_r, :numerator, :denominator, :rationalize, :gcd, :lcm, :gcdlcm, :+@, :eql?, :singleton_method_added, :coerce, :i, :remainder, :real?, :nonzero?, :step, :positive?, :negative?, :quo, :arg, :rectangular, :rect, :polar, :real, :imaginary, :imag, :abs2, :angle, :phase, :conjugate, :conj, :to_c, :between?, :instance_of?, :public_send, :instance_variable_get, :instance_variable_set, :instance_variable_defined?, :remove_instance_variable, :private_methods, :kind_of?, :instance_variables, :tap, :method, :public_method, :singleton_method, :is_a?, :extend, :define_singleton_method, :to_enum, :enum_for, :=~, :!~, :respond_to?, :freeze, :display, :object_id, :send, :nil?, :hash, :class, :singleton_class, :clone, :dup, :itself, :taint, :tainted?, :untaint, :untrust, :trust, :untrusted?, :methods, :protected_methods, :frozen?, :public_methods, :singleton_methods, :!, :!=, :__send__, :equal?, :instance_eval, :instance_exec, :__id__]
```

As you can see, you get a listing of all the methods on the number `1` that you could invoke. The names are prefixed with a colon (`:`) that you can safely ignore for now. If you find the results too muddled, you can easily sort them alphabetically. Try it for yourself - simply call the method sort on the result of methods:

```ruby
>> 1.methods.sort
=> [:!, :!=, :!~, :%, :&, :*, :**, :+, :+@, :-, :-@, :/, :<, :<<, :<=, :<=>, :==, :===, :=~, :>, :>=, :>>, :[], :^, :__id__, :__send__, :abs, :abs2, :angle, :arg, :between?, :bit_length, :ceil, :chr, :class, :clone, :coerce, :conj, :conjugate, :define_singleton_method, :denominator, :display, :div, :divmod, :downto, :dup, :enum_for, :eql?, :equal?, :even?, :extend, :fdiv, :floor, :freeze, :frozen?, :gcd, :gcdlcm, :hash, :i, :imag, :imaginary, :inspect, :instance_eval, :instance_exec, :instance_of?, :instance_variable_defined?, :instance_variable_get, :instance_variable_set, :instance_variables, :integer?, :is_a?, :itself, :kind_of?, :lcm, :magnitude, :method, :methods, :modulo, :negative?, :next, :nil?, :nonzero?, :numerator, :object_id, :odd?, :ord, :phase, :polar, :positive?, :pred, :private_methods, :protected_methods, :public_method, :public_methods, :public_send, :quo, :rationalize, :real, :real?, :rect, :rectangular, :remainder, :remove_instance_variable, :respond_to?, :round, :send, :singleton_class, :singleton_method, :singleton_method_added, :singleton_methods, :size, :step, :succ, :taint, :tainted?, :tap, :times, :to_c, :to_enum, :to_f, :to_i, :to_int, :to_r, :to_s, :truncate, :trust, :untaint, :untrust, :untrusted?, :upto, :zero?, :|, :~]
```

## Invoking methods with arguments
When talking to an object via its methods, it is possible to give it additional information so it can give you an appropriate response.

This additional information is called the "arguments to a method." The name "argument" makes sense if you stop to think about the fact that methods are the paths of communication between objects.

Here's an example of an argument to the method `index`, which finds the position of the argument in the array:

```ruby
>> ['rock','paper','scissors'].index('paper')
=> 1
```

Here, `index` is the method and `'paper'` the argument. If there is more than one argument, they can be passed to the method by simply separating them with commas.

Try using a method that takes two arguments - use the `between?` method to determine if the number `2` lies between the numbers `1` and `3`.

```ruby
>> 2.between? 1,3
=> true
```

[\[prev\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_ruby_objects/0_0_introduction_to_objects.md) 
[\[table of contents\]](https://github.com/Fahrenhei7/rubymonk/blob/master/README.md#ruby-primer)
[\[next\]](https://github.com/Fahrenhei7/rubymonk/blob/master/ruby_primer/introduction_to_ruby_objects/0_2_syntactic_sugar_for_special_methods.md)
