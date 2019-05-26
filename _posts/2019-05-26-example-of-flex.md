---
layout:     post
title:      Let's design some components using Flexbox properties for our web application! 
date:       2019-05-26
summary:    
categories: Developper skills
mathjax: true
---

Le meilleur moyen de comprendre les propriétés "Flexbox" est de le voir en cas pratique, donc par ici:


# Card 
<html>
<body>
	<div class="pizza">
 		 <div class="pizza__herro">
   			 <img src="https://images.unsplash.com/photo-1474600056930-615c3d706456?ixlib=rb-1.2.1&auto=format&fit=crop&w=1052&q=80" alt="pizza" class="pizza__img">
 		 </div>
 				 <div class="pizza__content">
    				<div class="pizza__title">
      					<h1 class="pizza__heading">Pizza Végétarienne 👌</h1>
      						<div class="pizza__tag pizza__tag--1">#vegetarian</div>
      							<div class="pizza__tag pizza__tag--2">#italian</div>
    						</div>
    					<p class="pizza__description">Une délicieuse pizza veggie composé d'une sauce tomate maison, mozzarella, champignons, oignons rouges, olives & origan </p>
    <div class="pizza__details">
      <p class="pizza__detail"><span class="emoji">🍕</span>850 kcal</p>
      <p class="pizza__detail"><span class="emoji">⏱</span>30 min</p>
      <p class="pizza__detail"><span class="emoji">⭐</span>4.7 / 5</p>
    </div>
  </div>
  <div class="pizza__price">$11.99</div>
</div>
</body>
</html>


<style>
	
.pizza {
  display: flex;
  max-width: 800px;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 30px 80px 10px rgba(0, 0, 0, 0.2);
  
}

.pizza__herro {
  flex: 0 0 45%;
}

.pizza__img {
  width: 100%;
  height: 100%;
}

.pizza__content {
  flex: 1;
  background-color: white;
  padding: 35px 30px;
  display: flex;
  flex-direction: column;
}

.pizza__price {
  flex: 0 0 50px;
  background: linear-gradient(to bottom, #67b26f, #4ca2cd);
  color: white;
  writing-mode: vertical-rl;
  display: flex;
  align-items: center;
  justify-content: center;
}

.pizza__title {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}
.pizza__heading {
  font-size: 20px;
  flex: 1;
  margin-right: auto;
}

.pizza__tag {
  font-size: 10px;
  text-transform: uppercase;
  padding: 2px 7px;
  margin-left: 7px;
  border-radius: 100px;
}

.pizza__tag--1 { background-color: #67b26f; }
.pizza__tag--2 { background-color: #4ca2cd; }
.pizza__description {
  font-size: 14px;
}

.pizza__details {
  display: flex;
  margin-top: auto;
}

.pizza__detail {
  font-size: 15px;
  text-transform: uppercase;
  margin-right: 20px;
  font-weight: 700;
  display: flex;
  align-items: center;
}
.emoji {
  font-size: 18px;
  margin-right: 3px;
}

</style>

---


## HTML

```html
<div class="pizza">
 	<div class="pizza__herro">
   		<img src="https://images.unsplash.com/photo-1474600056930-615c3d706456?ixlib=rb-1.2.1&auto=format&fit=crop&w=1052&q=80" alt="pizza" class="pizza__img">
 	</div>
 		<div class="pizza__content">
    		<div class="pizza__title">
      			<h1 class="pizza__heading">Pizza Végétarienne 👌</h1>
      				<div class="pizza__tag pizza__tag--1">#vegetarian</div>
     					 <div class="pizza__tag pizza__tag--2">#italian</div>
    				 		</div>
    							<p class="pizza__description">Une délicieuse pizza veggie composé d'une sauce tomate maison, mozzarella, champignons, oignons rouges, olives & origan </p>
   					 				<div class="pizza__details">
											<p class="pizza__detail"><span class="emoji">🍕</span>850 kcal</p>
												<p class="pizza__detail"><span class="emoji">⏱</span>30 min</p>
									 				<p class="pizza__detail"><span class="emoji">⭐</span>4.7 / 5</p>
   									  			</div>
 								  			</div>
 							  			 <div class="pizza__price">$11.99</div>
						   			</div>
```

---

## CSS

```css

.pizza {
  display: flex;
  max-width: 900px;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 30px 80px 10px rgba(0, 0, 0, 0.2);
  
}

.pizza__herro {
  flex: 0 0 45%;
}

.pizza__img {
  width: 100%;
  height: 100%;
}

.pizza__content {
  flex: 1;
  background-color: white;
  padding: 35px 30px;
  display: flex;
  flex-direction: column;
}

.pizza__price {
  flex: 0 0 50px;
  background: linear-gradient(to bottom, #67b26f, #4ca2cd);
  color: white;
  writing-mode: vertical-rl;
  display: flex;
  align-items: center;
  justify-content: center;
}

.pizza__title {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}
.pizza__heading {
  font-size: 20px;
  flex: 1;
  margin-right: auto;
}

.pizza__tag {
  font-size: 10px;
  text-transform: uppercase;
  padding: 2px 7px;
  margin-left: 7px;
  border-radius: 100px;
}

.pizza__tag--1 { background-color: #67b26f; }
.pizza__tag--2 { background-color: #4ca2cd; }
.pizza__description {
  font-size: 14px;
}

.pizza__details {
  display: flex;
  margin-top: auto;
}

.pizza__detail {
  font-size: 15px;
  text-transform: uppercase;
  margin-right: 20px;
  font-weight: 700;
  display: flex;
  align-items: center;
}
.emoji {
  font-size: 18px;
  margin-right: 3px;
}

```

---