---
layout:     post
title:      Building a UI Component for better design
date:       2019-05-07
summary:    
categories: Developper skills
mathjax: true
---

Learn how *Uber*, *Shopify* and *Airbnb* are leveraging components to build a consistent **UI/UX design system.**
![airBnB](/images/airBnB.png)

Components are a great way to design and develop your UI using smaller, reusable pieces with better consistency.

<blockquote>
  <p>
In today’s ecosystem, UI components can also function as UX components, combining the power to create both functional and visual consistency.
						</p>
  <footer><cite title="UI/UX">Jonathan Saring</cite></footer>
</blockquote>

You can design some compenents, then reuse them to build your *own product very quickly*. So let's *design*!

## *"UI kit"* : *In this article, I'll show you some compenents, designed by myself*
> *Most of the components have a dependency on [Bootstrap (4.3)](https://getbootstrap.com/) & [Fontawesome (5.7)](https://fontawesome.com/), so make sure you have the libraries in your project.*


# Avatar & Button design:

So let's begin with a simple one, useful for your *profile* for example.


![avatar](/images/ladies.png)

---
## HTML
```ruby
	<div class="container">
		<h2>Avatar design</h2>
      		<img src="./ladies.jpeg" alt="" class="avatar">
      		 <img src="./ladies.jpeg" alt="" class="avatar-small">
     </div>
```
## CSS
```ruby
.avatar {
  border-radius: 50%;
  width: 70px;
}

.avatar-small {
  border-radius: 50%;
  width: 50px;
}
```

---

Then, **Button**, I choose to design two kind of button, [*Medium*](https://medium.com/) and [*Treehouse*](https://teamtreehouse.com/).

---
<html>
<div class="container">
    <h2>Button design</h2>
       <a href="#" class="btn-medium">Write stories</a>
         <a href="#" class="btn-treehouse">Free trial</a>
     </div>
<style>.btn-medium {
  color: #999999;
  border: 1px solid #999999;
  padding: 10px 15px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
}

.btn-medium:hover {
  opacity: 1;
  text-decoration: none;
  color: #999999;
}

.btn-treehouse {
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  font-weight: bold;
  background: #6AD58B;
  opacity: 0.8;
}

.btn-treehouse:hover {
  opacity: 1;
  background: #6AD58B;
  text-decoration: none;
  color: white;
}</style>
</html>


>**Tips** Custom them to make your own *"style"* for your website.



*Let's code!* [*Try it here*](https://codepen.io/andryjohn/pen/gJpQeq)

---
## HTML
```ruby
	<div class="container">
		<h2>Button design</h2>
     	 <a href="#" class="btn-medium">Write stories</a>
         <a href="#" class="btn-treehouse">Start now</a>
     </div>

```
## CSS

```ruby
.btn-medium {
  color: #999999;
  border: 1px solid #999999;
  padding: 10px 15px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
}

.btn-medium:hover {
  opacity: 1;
  text-decoration: none;
  color: #999999;
}

.btn-treehouse {
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  font-weight: bold;
  background: #6AD58B;
}

.btn-treehouse:hover {
  opacity: 1;
  background: #6AD58B;
  text-decoration: none;
  color: white;
}
```

---

# Cards design: 

Let's move on! The next one is, **cards**


![card](/images/cards.png)

*Let's code!* [*Try it here*](https://codepen.io/andryjohn/pen/MdaOEY)

---

## HTML

``` ruby
  <h2>Card design</h2>
      <div class="row">
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
      </div>
```

## CSS

```ruby
.card {
  position: relative;
  height: 175px;
  background: linear-gradient(-225deg, rgba(30,30,30,0.6) 30%, rgba(46,46,46,0.5) 80%), url("http://unsplash.it/400/300/?random");
  background-size: cover;
  color: white;
}

.card-user {
  border-radius: 50%;
  position: absolute;
  top: 10px;
  right: 10px;
}
.card-category {
  position: absolute;
  top: 10px;
  left: 10px;
}
.card-description {
  position: absolute;
  bottom: 10px;
  left: 10px;
}
```

---

# Banner:

We've almost done, the last one is  **Banner**. Great for building your *landing page*!

![banner](/images/Banner.png)

*Let's code!* [*Try it here*](https://codepen.io/andryjohn/pen/EzVoWQ)

---

## HTML
```ruby
<h2>Banner design</h2>
      <div class="banner">
        <div class="banner-content">
          <h1>Coding Bootcamp in Paris</h1>
          <p>Change your life and learn to code this summer</p>
          <a href="#" class="btn-treehouse">Start Now</a>
        </div>
      </div>
```

## CSS
```ruby
.banner {
  display: flex;
  height: 100vh;
  background: linear-gradient(-225deg, rgba(30,30,30,0.6) 30%, rgba(46,46,46,0.5) 80%), url("http://unsplash.it/400/300/?random");
  background-size: cover;
  color: white;
  text-align: center;
  align-items: center;
  justify-content: space-around;
}

.banner h1 {
  font-size: 35px;
  font-weight: bolder;
}

.banner p {
  font-size: 15px;
  font-weight: lighter;
}
```

---

Ok, we're done, just in case, when a component is needed in a specific part of a specific app, it might need some adjustments and modifications. 
All the source code are available on my github account [right here](https://github.com/andryjohn/UI-sprint) 


  <footer><cite title="Workshop">Credit: Andry Rajohnson from "workshop le wagon UI"</cite></footer>

---