---
layout:     post
title:      Tower of Hanoi in Ruby
date:       2019-05-05
summary:   Solving the Tower of Hanoi Algorithm
categories: Developper skills
mathjax: true
---

![Tower of Hanoi](/images/Tower_of_Hanoi_4.gif)

The objective of the game is to move the entire stack to another rod, obeying the following simple rules:

>1. Only one disk can be moved at a time.
2. Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack or on an empty rod.
3. No larger disk may be placed on top of a smaller disk.

### Example

**Imput**

I take an integer as a input, that represents the number of disks. Let’s say 2.

**Output**

I need to have the steps (the moves) of each disk to know how to solve the Tower of Hanoi:

```ruby
# Move from A to C
# Move from A to B
# Move from C to B 
```
### Explanation

I move the first disk (so the smallest) from A to C. Then I can place the biggest disk directly to the destination rod (B). And then, place the smallest (waiting in C) on top of the biggest in B.

### Code
```ruby 
def hanoi_tower(n, source = 'A', destination = 'B', auxiliary = 'C')
  return unless n

  if n == 1
    puts "Move from #{source} to #{destination}"
  else
    # Step 1 − Move n-1 disks from source to aux
    hanoi_tower(n-1, source, auxiliary, destination)

    # Step 2 − Move nth disk from source to dest
    puts "Move from #{source} to #{destination}"

    # Step 3 − Move n-1 disks from aux to dest
    hanoi_tower(n-1, auxiliary, destination, source)
  end
end

hanoi_tower(1)
# Move from A to B

hanoi_tower(2)
# Move from A to C
# Move from A to B
# Move from C to B

# What it does when n == 2:
# it calls `hanoi_tower(1, source, auxiliary, destination)`
# but as n==1, it puts "Move from #{source} to #{destination}"
# so: Move from A to C
# then it puts "Move from #{source} to #{destination}"
# so: Move from A to B
# then it calls `hanoi_tower(1, auxiliary, destination, source)` (parameters are in different order)
# so: Move from C to B

hanoi_tower(3)
# Move from A to B
# Move from A to C
# Move from B to C
# Move from A to B
# Move from C to A
# Move from C to B
# Move from A to B
```