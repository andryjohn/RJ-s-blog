---
layout:     post
title:      Learn how to create video popup with Magnific Popup!
date:       2019-05-31
summary:    
categories: Developper skills
mathjax: true
---
![video](/images/video.jpeg)
>Excellent content is important but sometimes words on a page aren't as impactful as imagery. Pop up video elements can do wonders for both giving your website a human voice while also showcasing a more visually engaging element to your website

Video remains one of the most popular forms of content marketing around -- and it's certainly one of the most beneficial for a website.
This is a simple example with basic HTML/CSS and JS method, to insert mp4 video in your website. Enjoy!


## HTML 

---

```html
<div class="container">
<div id="light">
  <a class="boxclose" id="boxclose" onclick="lightbox_close();"></a>
  <video id="VisaChipCardVideo" width="1080" controls>
      <source src="" type="video/mp4">
      <!--Browser does not support <video> tag -->
    </video>
</div>

<div id="fade" onClick="lightbox_close();"></div>

<div class="icons">
  <a href="#" class="fas fa-play-circle" onclick="lightbox_open();"> See a Demo </a>
  </div>
  </div> 
```

## CSS

---

```css
.container{
  display: flex;
  justify-content: center;
  font-size: 5em;
  font-weight: lighter;
}
a {
  text-decoration: none;
  color: #EF5E46;
  opacity: 0.6;
  
}
a:hover {
  text-decoration: none;
  opacity: 1;
  color: #EF5E46;
}
#fade {
  display: none;
  position: fixed;
  top: 0%;
  left: 0%;
  width: 100%;
  height: 100%;
  background-color: #001628;
  z-index: 1001;
  -moz-opacity: 0.8;
  opacity: .80;
  filter: alpha(opacity=80);
}


#light {
  display: none;
  position: absolute;
  top: 50%;
  left: 50%;
  max-width: 600px;
  max-height: 360px;
  margin-left: -550px;
  margin-top: -350px;
  z-index: 1002;
  overflow: visible;
}

```

## JAVASCRIPT

---

```js
window.document.onkeydown = function(e) {
  if (!e) {
    e = event;
  }
  if (e.keyCode == 27) {
    lightbox_close();
  }
}

function lightbox_open() {
  var lightBoxVideo = document.getElementById("VisaChipCardVideo");
  window.scrollTo(0, 0);
  document.getElementById('light').style.display = 'block';
  document.getElementById('fade').style.display = 'block';
  lightBoxVideo.play();
}

function lightbox_close() {
  var lightBoxVideo = document.getElementById("VisaChipCardVideo");
  document.getElementById('light').style.display = 'none';
  document.getElementById('fade').style.display = 'none';
  lightBoxVideo.pause();
}
````

---

<h2><a href="https://codepen.io/andryjohn/pen/xNWvdo"> See a demo</a> on codepen</h2>


<footer><cite title="Workshop">Credit: Andry Rajohnson</cite></footer>