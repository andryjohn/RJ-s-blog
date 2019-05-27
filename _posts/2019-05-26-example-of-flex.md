---
layout:     post
title:      Let's design some components using Flexbox properties for our web application! 
date:       2019-05-26
summary:    
categories: Developper skills
mathjax: true
---

Le meilleur moyen de comprendre les propriétés "Flexbox" est de le voir en cas pratique, cet article complète [celle-ci.](https://rajohnson-andry.tk/developper/skills/2019/05/08/composants-design/)


## Card 

Le design de carte est éxercice parfait pour illustrer les propriétés "Flexbox"

---

![pizza](/images/pizza.png)

---

[Test yourself!](https://codepen.io/andryjohn/pen/XwqBOZ)

### HTML

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

### CSS

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

## Card with nice hover effect: 

Ici, on reste sur les "cards", mais on va y ajouté un effet de hover assez sympa!


<a href="https://codepen.io/andryjohn/pen/QREPVe">Test Yourself!</a>

---


<body>
<div class="hero-section">
  <div class="card-grid">
    <a class="card" href="#">
      <div class="card__background" style="background-image: url(https://images.unsplash.com/photo-1556742502-ec7c0e9f34b1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80)"></div>
      <div class="card__content">
        <p class="card__category">Stripe</p>
        <h3 class="card__heading">Cool API</h3>
      </div>
    </a>
    <a class="card" href="#">
      <div class="card__background" style="background-image: url(https://images.unsplash.com/photo-1531746790731-6c087fecd65a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=995&q=80)"></div>
      <div class="card__content">
        <p class="card__category">Machine</p>
        <h3 class="card__heading">Join us</h3>
      </div>
    </a>
    <a class="card" href="#">
      <div class="card__background" style="background-image: url(https://images.unsplash.com/photo-1516638022313-53fa45a84c7f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80)"></div>
      <div class="card__content">
        <p class="card__category">Design</p>
        <h3 class="card__heading">Get inspired</h3>
      </div>
    </li>
    <a class="card" href="#">
      <div class="card__background" style="background-image: url(https://images.unsplash.com/photo-1491933382434-500287f9b54b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1900&q=80)"></div>
      <div class="card__content">
        <p class="card__category">Apple</p>
        <h3 class="card__heading">An Ecosystem</h3>
      </div>
    </a>
  <div>
</div>


<style>
.hero-section{
  align-items: flex-start;
  display: flex;
  min-height: 100%;
  justify-content: center;
  padding: 64px 24px;
}

.card-grid{
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  grid-column-gap: 10px;
  grid-row-gap: 10px;
  max-width: 1200px;
  width: 100%;
  border-radius: 25px;
}

@media(min-width: 540px){
  .card-grid{
    grid-template-columns: repeat(2, 1fr); 
  }
}

@media(min-width: 960px){
  .card-grid{
    grid-template-columns: repeat(4, 1fr); 
  }
}

.card{
  list-style: none;
  position: relative;
  border-radius: 15px;
}

.card:before{
  content: '';
  display: block;
  padding-bottom: 150%;
  width: 100%;
}

.card__background{
  background-size: cover;
  background-position: center;
  border-radius: 24px;
  bottom: 0;
  filter: brightness(0.75) saturate(1.2) contrast(0.85);
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transform-origin: center;
  trsnsform: scale(1) translateZ(0);
  transition: 
    filter 200ms linear,
    transform 200ms linear;
}

.card:hover .card__background{
  transform: scale(1.05) translateZ(0);
}

.card-grid:hover > .card:not(:hover) .card__background{
  filter: brightness(0.5) saturate(0) contrast(1.2) blur(20px);
}

.card__content{
  left: 0;
  padding: 24px;
  position: absolute;
  top: 0;
}

.card__category{
  color:white;
  font-size: 0.8rem;
  margin-bottom: 8px;
  text-transform: uppercase;
}

.card__heading{
  color: white;
  font-size: 1.4rem;
  text-shadow: 2px 2px 20px rgba(0,0,0,0.2);
  line-height: 0.9;
  word-spacing: 100vw;
}
</style>


