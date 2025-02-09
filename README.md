# Ruby Immutability Issue with Getter Methods

This repository demonstrates a common mistake in Ruby where an object's internal state is unintentionally treated as immutable, even when it shouldn't be.  The issue arises when one only defines a getter method but forgets to define a setter method, making external changes to the object's state impossible.

## Bug
The `bug.rb` file shows a `MyClass` which intends to hold a value. However, attempting to change the `value` using `my_object.value = 20` fails because the code lacks a setter method. The object's internal `@value` remains unchanged.

## Solution
The `bugSolution.rb` file demonstrates the solution by adding a setter method to the class, making the internal state of the object modifiable.