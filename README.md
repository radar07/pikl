# Pikl - Interpreter written in Go

> This language is based on the Lox programming language implemented in the book
> **[Crafting Interpreters](https://craftinginterpreters.com/)** by **Robert Nystrom**

Language design

```go
// Statements
print "Hello, world!";

// Variables
var foo = "bar";
print foo;

// Control flow
if (true) {
  print "Yes";
} else {
  print "No";
}

var i = 0;
while (i < 5) {
  print(i)
  i++;
}

for (var i = 0; i < 5; i++) {
  print(i)
}

// Functions
fun print_sum(a, b) {
  return a+b;
}

print_sum(2, 3)

// Closures
fun add_pair(a, b) {
  return a + b;
}

fun print_sum(sum) {
  return sum;
}

print print_sum(add_pair)(2, 3) // Prints 5

// Classes
class Dog {
  sound() {
    print "Woof!"
  }

  serve(name) {
    print "It belongs to " + name + "!"
  }
}


var scooby = Dog();
print scooby;
scooby.sound();

class Lunch() {
  init(name) {
    this.name = name;
  }

  price() {
    print "Enjoy your " + this.name + " and dessert."
  }
}

var burger = Lunch("Cheesy burger");

class Brunch < Lunch {
  init() {
    super.name = name
    this.price = price
  }
}
```
