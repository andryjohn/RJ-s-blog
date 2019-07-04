---
layout:     post
title:      Classes & Objects in Ruby
date:       2019-05-15
summary:
categories: Developper skills
mathjax: true
---
![classe](/images/classe.jpeg)
>In a ruby application we have many objects ! As we often read, “Everything in Ruby is an Object”

**Classes and Objects** are very important concept in Ruby.

*Ruby* is an awesome language, because it use a different types of data inside of our program (strings, number, integers, boolean...).

*The problem* is, lot of things in a real world can't be represent with just a "string" or a "number" ( like credit card, a computer,..)

So, *Ruby* allows us to create our own datatype that called 'Classes'.

 Classes are basically just "a custom datatype" inside of our program, modelling a real world entities (Book, computer,...)


```ruby
class Book
	#givin attribute; all book gonna have title, author, pages
	attr_accessor :title, :author, :pages
end
#here we create a new book object
book1 = Book.new()
book1.title = "Harry Potter"
book1.author = "J.K Rowling"
book1.pages = 400
book2 = Book.new()
book2.title = "Lord of Ring"
book2.author = "Tolken"
book2.pages = 600

```
Ok, that cool! We've create two books, but there're a lot of lines for just a few objects.

### Initialize Method
Now, I'll introduce you to a "Initialize Method";

```ruby
class Book
	attr_accessor :title, :author, :pages
	def initialize(title, author, pages)
		@title = title
		@author = author
		@pages = pages


  end
end
#here we create a new book1 object with less codes
book1 = Book.new("Harry Potter", "J.K Rowling",400)
book2 = Book.new("Lord of Ring","Tolken", 600)

puts book1.author
```

Run the console: it work!

![result](/images/ruby.png)

### Object Method

Let's continue with "Object Method"

>"Imagine, you working in a college and you need a program to figure out if particular student have honor or not and **rules for 'having honor or not' constantly change.**
You need to write a method inside of our class, and that method are be able to tell us which specific student has honor"

```ruby
class Student
	attr_accessor :name, :major, :gpa
	def initialize(name, major, gpa)
		@name = name
		@major = major
		@gpa = gpa
	end
#define a object method
  def has_honor
  	if @gpa >= 16
   return true
   end
   return false
end

student1 = Student.new("Pierre", "Economy", 14.5)
student2 = Student.new("Chloé", "Art", 17.5)

puts student1_has honor

```

Run the console:

![result](/images/ruby2.png)

```ruby

...

student1 = Student.new("Pierre", "Economy", 14.5)
student2 = Student.new("Chloé", "Art", 17.5)

puts student2_has honor
```
Run the console:

![result](/images/ruby3*.png)
<footer><cite title="git">Credit: Andry RAJOHNSON</cite></footer>

