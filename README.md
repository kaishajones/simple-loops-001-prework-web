---
tags: intro, loop, times, while, until, for
languages: ruby
resources: 6
---
# Simple Looping

## Introduction

In software development, what construct gives an app a lot of power and flexibility? It's the ability to loop through things. If we had to manually go through and manipulate every element one by one, that would be an overly tedious task. So today we're going to go through 5 unique loop constructs: `loop`, `times`, `while`, `until`, and `for`.

## Loop

The first construct is `loop`. This is the simplest looping construct that we have in Ruby. It simply executes a block (the code that is between the `do` and `end` keywords). Try this in IRB in your Terminal:

```ruby
loop do
  puts "I have found the Time Machine!"
end
```

This will output `I have found the Time Machine!` an infinite number of times in your Terminal. Use Command + C to break out of the loop in your terminal.

## Times

The next construct is `times`. There are two important distinctions to be mindful of when using `times`. The first one is that it has to be called on an Integer (like 1 or 10000). The second is that it executes the block a certain number of times, which is dependent on the number that it's called on. Let's look at the example below:

```ruby
5.times do
  puts "Penguins like to jump off icebergs!"
end
```

This outputs `Penguins like to jump off icebergs!` five times in your Terminal.

## While

`While` is a little different from the first two constructs we looked at earlier. `While` will keep executing a block as long as a specific condition is `true`.

```ruby
iteration_counter = 1
while iteration_counter < 20
  puts "The current number is less than 20".
  iteration_counter += 1
end
```

As long as the condition `iteration_counter < 20` evaluates to true, the block will continue to execute. On each iteration, it will output `The current number is less than 20`, and it will increment the `iteration_counter` variable by 1. When counter is finally equal to 20, it will break out of the loop.

## Until

`Until` is simply the inverse of a `while` loop. An `until` keyword will keep executing a block until a specific condition is true.

```ruby
countdown_counter = 20
until countdown_counter == 0
  puts "There is still time left!"
  countdown_counter -= 1
end
puts "You're now out of time."
```

The `countdown_counter` starts at 20, and when the `until` loop starts executing the block, it evaluates whether `countdown_counter == 0`. If it is false, then it will output `There is still time left!`, and decrement the coundown_counter by 1. When the statement `countdown_counter == 0` evaluates to true, it will then output `You're now out of time.`.

## For

The final construct is the `for` loop. This is one of the more confusing loops in the Ruby language, so it's best to explain this one via an example:

```ruby
for counter in 1..40 do
  puts "The current number is #{counter}."
end
```

Before going into the `for` example, it's important to explain what `1..40` does. `1..40` is a [`Range`](http://www.ruby-doc.org/core-2.2.0/Range.html) object. A range represents an interval that starts with a beginning element, and ends with an end element. The range we have starts with a 1, and ends with a 40. Open up IRB in your Terminal, and type in `(1..40).to_a`. You're converting a Range object to an Array object, and it will return an array with all of the numbers that constitute the `1..40` range.

When the `for` keyword is executed, it sets `counter` equal to the first element of the range, which is 1. The first output of the `for` statement is `The current number is 1.`. It will keep going through the range until it reaches the last element, which is 40. What will be the output of the last element? `The current number is 40.`.

## Instructions

Code your solutions in `simple_looping.rb`. The first word of each method in that file corresponds to the loop construct that you should use. Happy coding!

Be sure to run `ironboard` to run the tests for this lab.

### One Hint to Keep in mind...

Look up what a `break` keyword does, and figure out how it will help you get othe `loop` test passing!

## Resources
- [Bastards Book](http://ruby.bastardsbook.com/) - [Loops](http://ruby.bastardsbook.com/chapters/loops/)
- [Ruby Docs](http://www.ruby-doc.org/) - [Loop](http://www.ruby-doc.org/core-2.2.0/Kernel.html#method-i-loop)
- [Ruby Docs](http://www.ruby-doc.org/) - [Times](http://www.ruby-doc.org/core-2.2.0/Integer.html#method-i-times)
- [Ruby Docs](http://www.ruby-doc.org/) - [While](http://www.ruby-doc.org/core-2.2.0/doc/syntax/control_expressions_rdoc.html#label-while+Loop)
- [Ruby Docs](http://www.ruby-doc.org/) - [Until](http://www.ruby-doc.org/core-2.2.0/doc/syntax/control_expressions_rdoc.html#label-until+Loop)
- [Ruby Docs](http://www.ruby-doc.org/) - [For](http://www.ruby-doc.org/core-2.2.0/doc/syntax/control_expressions_rdoc.html#label-for+Loop)
