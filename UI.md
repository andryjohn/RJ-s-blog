---
layout: default_UI
title: RJ's UI kit
tags: design
permalink: /design/
mathjax: true
---


>"99% du design d'une application web est contistué des mêmes composants, j'ai décidé d'en coder quelques uns et de vous les partagés!"

Ce sont des **"composants web"** que l'on trouve de manière **récurrents** sur nos **applications web** préférés, je vais en intégrer les principaux tels que l'avatar, les boutons, les bannières,... afin de vous les partagés et que vous puissiez les utilisés.

Les codes sont visible sur [codepen.io](https://codepen.io/dashboard/), pour chaques éléments, je vous renseigne le lien.

## *"UI kit"* :
> *La majorité des composants utilisent [Bootstrap (4.3)](https://getbootstrap.com/) & [Fontawesome (5.7)](https://fontawesome.com/), si vous décidez d'en utiliser un ou plusieurs , incorporez ces librairies à vos projets!*

## Avatar:

Ce composant simple, néamoins indispensable sur les profils de nos réseaux sociaux.

[*Voir le code*](https://codepen.io/andryjohn/pen/KjVzbw)

![avatar](/images/avatar.png)

## Buttons:

[*Voir le code*](https://codepen.io/andryjohn/pen/KjVzbw)

<div class="container-card">
  <a href="#" class="btn-medium">Write a stories</a>
  <a href="#" class="btn-treehouse">Free Trial</a>
  </div>
  <style>.btn-medium {
  color: #999999;
  border: 1px solid #999999;
  padding: 10px 15px;
  margin: px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
}
.btn-medium:hover {
  text-decoration: none;
  color: #999999;
  opacity: 1;
}

.btn-treehouse {
  border: 2px solid #4AB66A;
  padding: 10px 15px;
  color: #4AB66A;
  font-weight: bold;
  border-radius: 4px;
  opacity: 0.7;
}
.btn-treehouse:hover {
  text-decoration: none;
  color: #4AB66A;
  opacity: 1;
} </style>


## Alerts!

[*Voir le code*](https://codepen.io/andryjohn/pen/OYywBd)

<div class="flash flash-success alert alert-dismissible fade show" role="alert">
  <span><strong>Yay!</strong> 🎉 you successfully signed in to our service.</span>
</div>

<div class="flash flash-warning alert alert-dismissible fade show" role="alert">
  <span><strong>Mmh</strong> 🤔 seems like you don't have <a href="#">profile picture</a> yet.</span>
</div>

<div class="flash flash-danger alert alert-dismissible fade show" role="alert">
  <span><strong>Oops!</strong> 😱 a problem has occurred while processing your booking.</span>
</div>


<style>
.flash {
  padding: 16px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: whitesmoke;
  box-shadow: 0 0 8px rgba(0,0,0,0.2);
  border-radius: 4px;
  margin: 8px;
}

.flash-success {
  border: 2px solid #1EDD88;
}

.flash-warning {
  border: 2px solid #FFC65A;
}

.flash-danger {
  border: 2px solid #FD1015;
}
.flash:hover {
  webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  transition: 0.9s;

}
</style>


## Landing page:

[*Voir le code*](https://codepen.io/andryjohn/pen/EzVoWQ)

![Card](/images/landing-page.png)

## Card grid :

[*Voir le code*](https://codepen.io/andryjohn/pen/ZdQRmb)
<div class="row">
    <div class="col-xs-12 col-sm-4">
    <div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.3)), url('https://source.unsplash.com/hrlvr2ZlUNk');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Breakfast</h2>
    <p>Awesome place</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
    <div class="col-xs-12 col-sm-4">
  <div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.3)), url('https://source.unsplash.com/Pt_YmiYm7a4');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Brunch</h2>
    <p>Lovely place, "the best place"</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
    <div class="col-xs-12 col-sm-4">
<div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.3)), url('https://source.unsplash.com//D-vDQMTfAAU');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Asian Foods</h2>
    <p>Awesome place,we Love it!</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
</div>

<style>

.card {
  width: 15em;
  height: 8em;
  text-shadow: 0 1px 3px rgba(0,0,0,0.6);
  background-size: cover !important;
  background-position: center;
  color: whitesmoke;
  position: relative;
  border-radius: 7px;
  margin: 10px;
}
.card-user {
  position: absolute;
  right: 10px;
  top: 10px;
  width: 60px;
  border-radius: 50%;
  height: 55px;
}
.card-category {
  position: absolute;
  top: 10px;
  left: 10px;
  font-size: 15px;
  text-transform: uppercase;
}
.card-description {
  position: absolute;
  bottom: 10px;
  left: 10px;
}
.card-description h2 {
  font-size: 24px;
}
.card-description p {
  font-size: 14px;
  opacity: 0.7;
  font-weight: lighter;
  color: #ffff;
}
.card-link {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  z-index: 2;
  background: black;
  opacity: 0;
}
.card:hover {
   margin: 10px;
   webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  transition: 0.9s;
}

</style>


## Cards Netflix like:


[*Voir le code*](https://codepen.io/andryjohn/pen/xoOxVq)
<div class="container">
        <div class="box">
            <a href=""><img src="https://github.com/andryjohn/Netflix-Clone/blob/master/img/p1.PNG?raw=true" alt=""></a>
            <a href=""><img src="https://github.com/andryjohn/Netflix-Clone/blob/master/img/p2.PNG?raw=true" alt=""></a>
            <a href=""><img src="https://github.com/andryjohn/Netflix-Clone/blob/master/img/p3.PNG?raw=true" alt=""></a>
            <a href=""><img src="https://github.com/andryjohn/Netflix-Clone/blob/master/img/p4.PNG?raw=true" alt=""></a>
          </div>
      </div>

<style>
.container {
display: flex;
}
.box {
  display: grid;
  grid-gap: 5px;
  grid-template-columns: repeat(2, minmax(110px, 1fr));
}

.box a {
  transition: transform .3s;
}

.box a:hover {
  transition: transform .3s;
  -ms-transform: scale(1.4);
  -webkit-transform: scale(1.4);
  transform: scale(1.4);
}

.box img {
  border-radius: 3px;
   box-shadow: 0 0 15px rgba(0,0,0,0.2);
}
 </style>

## Card product :

[*Voir le code*](https://codepen.io/andryjohn/pen/XwmYqw)

<div class="card-product">
  <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=926&q=80">
  <div class="card-product-infos">
    <h2>Macbook Pro</h2>
    <p>Product description with <strong>relevant info</strong> only.</p>
    </div>
</div>
<style>


.card-product {
  margin: 35px;
  overflow: hidden;
  height: 120px;
  background: white;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  display: flex;
  align-items: center;
  cursor: pointer;
}

.card-product img {
  height: 100%;
  width: 120px;
  object-fit: cover;
}

.card-product h2 {
  font-size: 16px;
  font-weight: bold;
  margin: 0;
}

.card-product p {
  font-size: 12px;
  line-height: 1.4;
  opacity: .7;
  margin-bottom: 0;
  margin-top: 8px;
}

.card-product .card-product-infos {
  padding: 16px;
}

.card-product:hover {
  webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  transition: 0.8s;
}
</style>



## Card trip:

[*Voir le code*](https://codepen.io/andryjohn/pen/XwmYqw)

<div class="card-trip">
  <img src="https://source.unsplash.com/vO0hUESehtc">
  <div class="card-trip-infos">
    <div>
      <h2>Italia </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/MTZTGvDsHFY' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/DpPutJwgyW8">
  <div class="card-trip-infos">
    <div>
      <h2>Kyoto </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/ZHvM3XIOHoE' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/oqFHLfLFtmc">
  <div class="card-trip-infos">
    <div>
      <h2>Japan </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/ZHvM3XIOHoE' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <style>


.card-trip {
  margin: 35px;
  overflow: hidden;
  background: whitesmoke;
  box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

.card-trip > img {
  height: 200px;
  width: 100%;
  object-fit: cover;
}

.card-trip h2 {
  font-size: 17px;
  font-weight: bold;
  margin: 0;
}

.card-trip p {
  font-size: 12px;
  opacity: 0.7;
  margin: 0;
}


.card-trip .card-trip-infos {
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  position: relative;
}

.card-trip-infos .card-trip-user {
  position: absolute;
  right: 16px;
  top: -20px;
  width: 45px;
  border-radius: 50%;
}
.card-trip:hover {
   webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  transition: 0.9s;
}
  </style>




## Card category:

[*Voir le code*](https://codepen.io/andryjohn/pen/XwqBOZ)

<figure class="pizza">
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
                </figure>


 <style>


.pizza {
  max-width: 800px;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 30px 80px 10px rgba(0, 0, 0, 0.2);
  display: flex;
  height: 250px;
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
  padding: 10px 45px;
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
.pizza:hover {
 webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
  -ms-transform: scale(1.1);
  -o-transform: scale(1.1);
  transform: scale(1.1);
  transition: 0.6s;

}
</style>


## Contact form:

[*Voir le code*](https://codepen.io/andryjohn/pen/Wqxpox)
<form id="contact" action="" method="post">
    <h3>Get in Touch</h3>
    <fieldset>
      <input placeholder="Your name" type="text" tabindex="1" required autofocus>
    </fieldset>
    <fieldset>
      <input placeholder="Your Email Address" type="email" tabindex="2" required>
    </fieldset>
    <fieldset>
      <textarea placeholder="Type your message here...." tabindex="3" required></textarea>
    </fieldset>
    <fieldset>
      <button name="submit" type="submit" id="contact-submit" data-submit="...Sending">Submit</button>
    </fieldset>
  </form>

<style>
#contact input[type="text"],
#contact input[type="email"],
#contact input[type="tel"],
#contact input[type="url"],
#contact textarea,
#contact button[type="submit"] {
  font: 400 12px/16px "Roboto", Helvetica, Arial, sans-serif;
}

#contact {
  background: #F9F9F9;
  padding: 25px;
  margin: 90px 0;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2), 0 5px 5px 0 rgba(0, 0, 0, 0.24);
}

#contact h3 {
  display: block;
  font-size: 30px;
  font-weight: 300;
  margin-bottom: 10px;
}

#contact h4 {
  margin: 5px 0 15px;
  display: block;
  font-size: 13px;
  font-weight: 400;
}

fieldset {
  border: medium none !important;
  margin: 0 0 10px;
  min-width: 100%;
  padding: 0;
  width: 100%;
}

#contact input[type="text"],
#contact input[type="email"],
#contact input[type="tel"],
#contact input[type="url"],
#contact textarea {
  width: 100%;
  border: 1px solid #ccc;
  background: #FFF;
  margin: 0 0 5px;
  padding: 10px;
}

#contact input[type="text"]:hover,
#contact input[type="email"]:hover,
#contact input[type="tel"]:hover,
#contact input[type="url"]:hover,
#contact textarea:hover {
  -webkit-transition: border-color 0.3s ease-in-out;
  -moz-transition: border-color 0.3s ease-in-out;
  transition: border-color 0.3s ease-in-out;
  border: 1px solid #aaa;
}

#contact textarea {
  height: 100px;
  max-width: 100%;
  resize: none;
}

#contact button[type="submit"] {
  cursor: pointer;
  width: 100%;
  border: none;
  background: #4CAF50;
  color: #FFF;
  margin: 0 0 5px;
  padding: 10px;
  font-size: 15px;
}

#contact button[type="submit"]:hover {
  background: #43A047;
  -webkit-transition: background 0.3s ease-in-out;
  -moz-transition: background 0.3s ease-in-out;
  transition: background-color 0.3s ease-in-out;
}

#contact button[type="submit"]:active {
  box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.5);
}

#contact input:focus,
#contact textarea:focus {
  outline: 0;
  border: 1px solid #aaa;
}

::-webkit-input-placeholder {
  color: #888;
}

:-moz-placeholder {
  color: #888;
}

::-moz-placeholder {
  color: #888;
}

:-ms-input-placeholder {
  color: #888;
}
</style>


## Messages:

[*Voir le code*](https://codepen.io/andryjohn/pen/RmrrLd)

![Message](/images/messsage.png)



## Notification:

[*Voir le code*](https://codepen.io/andryjohn/pen/PvPVRj)

![Card](/images/notification.png)



## Footer:


[*Voir le code*](https://codepen.io/andryjohn/pen/PvPVRj)

![footer](/images/Footer.png)


D'autres liens sur RJ'blog:
*  [Mise en page avec flexbox et CSS grind!](https://rajohnson-andry.tk/developper/skills/2019/05/09/Top-site/)

 <footer><cite title="Workshop">Credit: Made by ©Andry Rajohnson, inspired by le wagon UI kit </cite></footer>

