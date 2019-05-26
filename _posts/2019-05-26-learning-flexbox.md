---
layout:     post
title:      Finally Understanding Flexbox with this tutorial!

date:       2019-05-26
summary:    
categories: Developper skills
mathjax: true
---

![Understanding flexbox - intro image](https://miro.medium.com/fit/c/1838/551/1*6-qimRY772NTcSJZ-o8SjQ.jpeg)

>Learning Flexbox can be a pain in the butt. For most persons, it's not particularly fun at first. It challenges you to rethink how you've dealt with layouts in css.

Don't fret. I really would walk you through all you need to know. So, let's get started.

## Why Use Flexbox?

CSS has evolved a lot over the past few years. Designers loved the introduction of filters, transitions, and transforms. But something was missing. Something we all craved.

Crafting Intelligent page layouts with CSS seemed to have persisted for too long, and this got many of us writing hacky CSS.

We always had to deal with floats, table display hacks, and the consequences they brought. If you’ve written CSS for sometime, you can probably relate to this. And if not, welcome to a better world!

It seems like our prayers as designers and front-end developers have finally been heard. This time, in grand style.

Now we can all ditch those hacky CSS tricks. No more incessant use of floats, table-cell displays.

It’s time to embrace a cleaner modern syntax for crafting intelligent layouts. Welcome the CSS Flexbox model.

## What Is Flexbox?

According to the specification, the flexbox model provides for an efficient way to layout, align, and distribute space among elements within your document, even when the viewport and the size of your elements is unknown and/or dynamic.  
If that sound too formal, I understand the feeling. In just a bit, I'll explain what that means in plain English.

Whether you write css in your dreams or you're just getting started, you'll feel right at home.

## How do I start using the flexbox model?

This is the first question everyone asks, and the answer is much simpler than you may have expected. To start using the Flexbox model, all you need to do is first define a **flex-container**.

Okay, did I make you more confused there? Let me explain. In regular html, laying out a simple list of items takes this form.

```html
<ul> <!--parent element-->
  <li></li> <!--first child element-->
  <li></li> <!--second child element-->
  <li></li> <!--third child element-->
</ul>
```

If you glanced at that, you must have seen that the unordered list houses the list elements. You'd call the `ul` the parent element, and the `li` the child element.

To use the flexbox model, you must make a parent element a **flex container** _(aka flexible container)_. You do this by setting `display: flex` or `display: inline-flex` for the inline variation. It's that simple, and from there you're all set to use the Flexbox model. Told you it wasn't as difficult as you expected.

![flexbox tip](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/flexbox-tip-1_zps6y7o7rc2.jpg)

Using an unordered list and a bunch of list elements, this is what that would bring us to.

```css
/*Make parent element a flex container*/
ul {
  display: flex; /*or inline-flex*/
}
```

I'm going to style the list items just a bit, so you may see what's going on here.

```css
li {
  width: 100px;
  height: 100px;
  background-color: #8cacea;
  margin: 8px;
}
```

And here is what we have:

![Flexbox kicks in](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_3_zpsytzach4m.png)

You may not have noticed, but something's happened already!

By default, "divs" in CSS stack vertically, from top to bottom.

![default link style](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_2_zpsjvonxs0e.png)

The image above is the result you may have hoped for. However, with the inclusion of that simple one-liner, `display:flex`, a change in layout is immediately seen. The list elements are now stacked horizontally, from left to right. Just like they would if you used float

![Flexbox kicks in](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_3_zpsytzach4m.png)

I really need you to follow along here. The Flexbox model kicks in as soon as you introduce the display property on any parent element. It's all started now.

You may not understand why that change in the orientation of the list elements came to be right now. I promise I'll go into the inner workings of that very soon. For now, blind trust would suffice. Simply understand that the inclusion of the display property starts off the Flexbox model.

There's one more thing I need to call your attention to. As soon as you set the display property to flex, the unordered list automatically becomes the **flex container** and the child elements (in this case, the list elements `li`) become **flex items**. These terms would come up over and over again as I walk you through some more interesting things the Flexbox model has in place.

I have used two key words, and I'd like to lay more emphasis on them. They are vital to understanding what lies ahead.

1.  Flex container : The parent element you've set `display: flex` on.
2.  Flex items : The children elements within a Flex container.

![flexbox tip 2](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/flexbox-tip-2_zpsgvnqmdhw.jpg)

This is the foundation for using the flexbox model, and as soon as that's understood, more interesting things lie ahead.

So, here is where I wrap up the Introduction to the Flexbox model.

---

## The Flex Container Properties

`Flex-direction || Flex-wrap || Flex-flow || Justify-content || Align-items || Align-content`

---
![Understanding flexbox - flex-container](http://i.imgur.com/xK4JUVX.jpg)

---

In the last article, I established some core principles. What flex-containers and flex-items are, and how to initiate the Flexbox model. Now is a good time to put all of that to good use. So, brace up.

Having set a parent element as a flex container, a couple of **alignment properties** are made available to be used on the flex container.  
Just like you'd define the width property on a block element as `width: 200px`, there are 6 different properties the flex container can take on, and defining these properties do NOT take a different approach.

### 1. Flex-direction

The `Flex-direction` property may take any of four values:, and it controls the direction in which the flex items are laid along the main axis.

```css
/*where ul represents a flex container*/
ul {
  flex-direction: row || column || row-reverse || column-reverse;
}
```

The `flex-direction` property let's us decide how the **flex items** are laid out. Either horizontally, vertically or reversed in both directions.  
Technically, horizontal and vertical isn't what it's called in the _"flex world"_. These are described as **main-axis** and **cross axis**, and the defaults are shown below:

![main axis](http://i.imgur.com/8DgaIMV.jpg)

By default, the `flex-direction` property is set to `row` and it aligns the flex-item(s) along the main axis. This explains what happened with our unordered list at the start of this article. Even though `flex-direction` property wasn't explicitly set, it took on the default value of `row` and so the flex items were laid across the main-axis, stacking horizontally from left to right.

### 2. Flex-wrap

The flex wrap property can take on any of three values:

```css
//where ul represents a flex container
ul {
  flex-wrap: wrap || nowrap || wrap-reverse;
}
```

Let's try sticking in a lot more list items within our unordered list. What do you think? Will our flex container resize or break up the list items?

```html
/*adding 3 more li elements*/
<ul> <!--parent element-->
  <li></li> <!--first child element-->
  <li></li> <!--second child element-->
  <li></li> <!--third child element-->
  <li></li>
  <li></li>
  <li></li>
</ul>
```

Fortunately, the flex-container adapts to accommodate our new flex-items

![Image of more children elements added to a flex container](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_4_zpsd860b8lu.png)

So let's go a bit further...Add a ridiculous amount of flex-items to our parent element. I choose 10 more items. What happens??

![Image of much more children elements added to a flex container](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_5_zpste0kkkru.png)

Again, the flex container adapts to fit all children in, even if I need to scroll my browser horizontally.  
This is the default behavior of every flex container. It keeps on accommodating more flex items on a single line because the `flex-wrap` property defaults to `nowrap`.

```css
ul {
  flex-wrap: nowrap; /*Keep on taking more flex items without breaking (wrapping)*/
}
```

Well, with that number of flex-items, you certainly want the flex-container to 'wrap' around these elements. i.e. When the available space can no longer support the flex-items, break unto multiple lines when needed, and with that comes the `wrap` value

```css
ul {
  flex-wrap: wrap;
}
```

With this, the flex items now break up into multiple lines when needed. In this case, when a single line can no longer contain all the list items in their default width, they break up into multiple lines. Even on resizing the browser!!

![Image of much more children elements now in multiple lines](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_6_zpscnqcf7my.png)

There's one more value, `wrap-reverse`. Yes, you guessed right. It lets the flex items break unto multiple lines but in the reverse direction.

![Image of much more children elements now in multiple lines with wrap-reverse](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_7_zpsi3w2os3q.png)

### 3. Flex-flow

The `flex-flow` is a shorthand property which takes `flex-direction` and `Flex-wrap` values. Ever used the `border` shorthand property? `border: 1px solid red`. It's the same concept here. Multiple values declared in one line.

Re-writing the code above would yield this:

```css
ul {
  flex-flow: row wrap; /*direction 'row' and yes, please wrap the items.*/
}
```

![image explaining the flex-flow property](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/flexbox-flex-flow_zpshybxvgcy.jpg)

Try out the other combinations this could take. `flex-flow: row nowrap`, `flex-flow: column wrap`, `flex-flow: column nowrap`
I'm sure you understand what those would produce. Give it a try.

### 4. Justify-content

Life's really good with the flexbox model! If you still doubt that, the justify-content property would convince you. It may take on any of these 5 values:

```css
ul {
  justify-content: flex-start || flex-end || center || space-between ||
    space-around;
}
```

And what exactly does the justify content property bring to the table? Well, It may remind you of the text-align property.

The justify content property defines how flex items are laid out on the main axis.

Consider the simple unordered list below:

```html
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
</ul>
```

Adding up some basic styling...

```css
ul {
  border: 1px solid red;
  padding: 0;
  list-style: none;
  background-color: #e8e8e9;
}

li {
  background-color: #8cacea;
  width: 100px;
  height: 100px;
  margin: 8px;
  padding: 4px;
}
```

We have this:

![initial](http://image.prntscr.com/image/a1aa457e10044a30b8fa3bd1d5fd4e31.png)

With the `justify-content property`, the three flex-items may be aligned across the main-axis in whatever way you desire. Here's the breakdown of what's possible.

Fist off, the default value, `flex-start`, groups all flex-items to the start of the main axis.

```css
ul {
  justify-content: flex-start;
}
```

![flex-start](http://i.imgur.com/Ct9Q1P5.png)

`flex-end` groups the flex-items to the end of the main axis.

```css
ul {
  justify-content: flex-end;
}
```

![flex-end](http://i.imgur.com/Rn3C5oL.png)

`Center` does just you'd expect - centering the flex items along the main axis.

```css
ul {
  justify-content: center;
}
```

![flex-center](http://i.imgur.com/kpm0rG0.png)

`Space-between` keeps the same space between each flex item.

```css
ul {
  justify-content: space-between;
}
```

![space-between](http://i.imgur.com/cUYgqJs.png)

Uhmm, did you notice anything different here? Take a look again:

![Understanding-Flexbox, Space between](http://i.imgur.com/lH5HtXV.jpg)

Finally, `space-around` keeps the same spacing around flex items.

```css
ul {
  justify-content: space-around;
}
```

![space-around](http://i.imgur.com/anlXv8t.png)

A second look doesn't hurt:

![Understanding-Flexbox, Space around](http://i.imgur.com/krodS0R.jpg)

Don't worry if these seem like too much to get a hold of. With a bit of practice you will get very comfortable with the syntax.

### 5. Align-items

The `align-items` property is somewhat similar to the `justify-content` property. Having understood the `justify-content` property, this should be easier to take in.

`Align-items` can be set to any of these values: flex-start || flex-end || center || stretch || baseline

```css
/*ul represents any flex container*/
ul {
  align-items: flex-start || flex-end || center || stretch || baseline;
}
```

It defines how flex-items are laid out on the **cross axis**. This is the difference between the `align-items` property and `justify-content`.

**The default value is `stretch`, and this will 'stretch' the flex-items so they fill the entire height of the flex container.**

![stretch](http://i.imgur.com/z6hibEr.png)

**The `flex-start` and `flex-end` properties do what you expect - group the items to the start or end of the cross-axis.**

![flex-start](http://i.imgur.com/7IWXXP3.png)

![flex-end](http://i.imgur.com/F0zDNT1.png)

**The `center` value is equally predictable. It aligns items to the center of the flex-container.**

![center](http://i.imgur.com/qSPeH9E.png)

**And the baseline value? It aligns flex-items along their baselines.**

![baseline](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_17_zpsovbaj6w0.png)

"Baseline" really sounds fancy. It appears to look just like `flex-start` but it is subtly different. What the heck is "baseline"? This should help:

![Understanding-Flexbox: Baseline](http://i.imgur.com/7vwt8Pb.jpg)

Isn't it awesome the amount of layout control you have here?

### 6. Align-content

Remember when you added more list elements to our unordered list? You got a multi-line flex container by using the `flex-wrap` property. The `align-content` property is used on multi-line flex-containers.

It takes the same values as `align-items` apart from `baseline`. By definition, it controls how the flex-items are aligned in a multi-line flex container. Just like `align-items`, the default value is also `stretch`

These are values you're familiar with. So, here's how they affect a multi-line flex-container.

**Stretch**

![stretch](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_18_zpsy8iaetza.png)

**Flex-start**

![flex-start](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_19_zpsdumnrbis.png)

**Flex-end**

![flex-end](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_20_zpsvtll0vn0.png)

**Center**

![center](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_21_zpsy0u5amdd.png)

...and that concludes this. You now understand how to use the various flex-container properties. Pretty soon, you'll need these to work through the practical sections coming up. I guess you're feeling much more confident now, right?

---

## The Flex Item Properties

`Order || Flex-grow || Flex-shrink || Flex-basis`

![Understanding flexbox - flex-item](http://i.imgur.com/7klPbEY.jpg)

In the previous article, we looked at flex containers and their alignment properties. Beautiful indeed. Sure you're getting a feel of what lies ahead now.
I'd take my focus off flex-containers now, and walk you through flex-items and their alignment properties.

Like flex-containers, a couple alignment properties are also made available on all flex-items. These are properties you can use on any children of a flex-container.
Let me walk you through them.

### 1. Order

The order property allows for reordering the flex items within a container. With the order property you can move a flex-item from one position to another. Just like you would do with sortable lists. This is done without affecting the source code. Which means the position of the flex items in the html source code isn't changed.

The default value for the order property is 0. It may take on either negative or positive values.

It's worth noting that flex items are reordered based on the number values of the order propery. From lowest to highest. For example :
Consider the unordered list below, containing 4 list items.

```html
<ul>
	<li>1</li>
	<li>2</li>
	<li>3</li>
	<li>4</li>
</ul>
```

By default, the flex items all have an `order` value of `0`. Just as you expected, you get this after some basic styling:

![default](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_22_zpspzuplcpn.png)

The Flex items displayed just as specified in the html source order.

What if for some reason, you wanted the first flex item to appear last? Without changing the source order in the html document?

Without changing the source order means you do not get to do this:

```html
<ul>
	<li>2</li>
	<li>3</li>
	<li>4</li>
	<li>1</li>
</ul>
```

Now that's where the `order` property comes in.
All you need to do is make the `order` value of flex item number 1 higher than that of other list items. (If you ever used the `z-index` property on block elements, you'd be familiar with this sort of thing)

````css
/*select first li element within the ul */
li:nth-child(1) {
  order: 1; /*give it a value higher than 0. Remember it's ```order:0``` for other flex-items by default*/
}
````

The flex items are then re-ordered from lowest to highest. Do not forget that list items 2, 3, and 4 all have the order value of 0. `order: 0`. Flex-item 1 has an order value of 1. `order: 1`.

![one](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_23_zpsh8wuweny.png)

Flex-items 2, 3, and 4 all have an order value of 0. So, the html source order is kept - no modifications made to the default display.

Sure you got that!

What if you gave flex-item 2 an order value of 2? Yes, you guessed right. It goes up the stack too, since it now represents the flex-item with the highest `order` value.

![one and two](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_24_zpss9yeoaap.png)

And what happens when two flex items have the same order value?
In the example below, flex-item 1 and 3 are given the same `order values`.

```css
li:nth-child(1) {
  order: 1;
}

li:nth-child(3) {
  order: 1;
}
```

![one and three](http://i1064.photobucket.com/albums/u363/Ohans_Emmanuel/flexbox-article/Screenshot_25_zpsu0aodhvy.png)

The items are still arranged from lowest to highest, but this time, flex-item 3 appears last because it comes after flex-item 1 in the source file (html document).

NB: The re-ordering is based on the positions in the source file, when two or more flex items have the same order value.

That was a lot of explanation. Let's move on to some other properties.

### 2. Flex grow and flex shrink

The beauty of flex items is being "flexible". The `flex-grow` and `flex-shrink` properties allow us play around this 'flexibility' even more.

The `flex-grow` and `flex-shrink` properties control how much a flex-item should "grow" (extend) if there are extra spaces, or "shrink" if there are no "extra" spaces. They may take up any values ranging from 0 to any positive number. `0 || positive numbers`

Let me demystify that. Consider the simple unordered list comprising just one list item:

```html
<ul>
	<li>I am a simple list</li>
</ul>
```

```css
ul {
  display: flex;
}
```

With a bit more styling, it appears like this.

![Flex grow](http://i.imgur.com/Ru6GV3r.png)

By default, the `flex-grow` property is set to `0`. By implication, the flex-item does NOT grow to fit the entire space available. The value `0` is like a "turn-off" switch. The `flex-grow` switch is turned off. However, if you changed the `flex-grow` value to `1`, here's what happens.

![Flex grow- 2](http://i.imgur.com/msa3JIS.png)

The flex-item now 'grows' to occupy all the available space. The switch's turned on! If you tried resizing your browser, the flex-item would also 'shrink' to accomodate the new screen size. Why? By default, the `shrink` property is set to 1. Which means the `flex-shrink` switch is also turned on!

I hope that doesn't feel like a short intro you cant wrap your head around. I'll take a closer look at the `flex-grow` and `flex-shrink` properties in a bit if you still don't get it.

Let's move on.

### 3. Flex basis

Remember how I said the beauty of the flex-items is being "flexible"? Well, it appears you also have a control over that. How cool.

The `flex-basis` property specifies the **initial** size of a flex-item. Before the `flex-grow` or `flex-shrink` properties adjust it's size to fit the container or not.

The previous statement is really important- so I'm taking a moment to reinforce that.

The default value is `flex-basis: auto`. `Flex-basis` can take on any values you'd use on the normal width property. That is, `percentages || ems || rems || pixels` etc

> Nb: when trying to set the basis property to a zero based value, Use the unit also. e.g. Use `flex-basis: 0px` not just `flex-basis: 0`

I'd bring back the 'one list' example here again.

```html
<ul>
	<li>I am a simple list</li>
</ul>
```

```css
ul {
  display: flex;
}

li {
  padding: 4px; /*some breathing space*/
}
```

By default, the initial width of the flex item is influenced by the default value, `flex-basis: auto`. The width of the flex-item is computed "automatically" based on the content size (and obviously, plus whatever padding you set too).

![Flex-basis](http://i.imgur.com/QzR7xhP.png)

This means if you increased the content in the flex-item, it automatically resizes to fit.

```html
<ul>
	<li>I am a simple list AND I am a simple list</li>
</ul>
```

![flex-basis-2](http://i.imgur.com/NVu6Q5e.png)

If you however want to set the flex-item to a fixed width, you also can!

```css
li {
  flex-basis: 150px;
}
```

Now the flex-item has been constrained to a width of 150px

![flex-item-3](http://i.imgur.com/72kMsE1.png)

It's getting even more interesting.

### 4. The flex shorthand

The `flex` shorthand allows us set the `flex-grow`, `flex-shrink` and `flex-basis` properties all at once. When appropriate, I advice you set all three properties at once using the flex shorthand than doing so individually.

```css
li {
  flex: 0 1 auto;
}
```

This code above is equal to setting the three properties: `flex-grow: 0; flex-shrink: 1; flex-basis: auto` Please note the order. `Flex-grow` first, then `flex-shrink`, and then `flex-basis`. The acronym GSB may help.

What happens if you fail to set one of the values in the flex-shorthand?
If you set only the `flex-grow` and `flex-shrink` values, `flex basis` would default to zero. This is called an _absolute flex_. And when you set only the `flex-basis`, you get a _relative flex_.

```css
//this is an absolute flex item
li {
  flex: 1 1; //flex-basis defaults to 0;
}

//this is a relative flex item
li {
  flex-basis: 200px; //only flex-basis is set
}
```

I know what you're thinking. What's the purpose of the relative and absolute flex? I answer that question later in this article.

For now, let's take a look at some useful flex shorthand values.

### 1. `flex: 0 1 auto`

```css
//again, the 'li' represents any flex-item
li {
  flex: 0 1 auto;
}
```

This is same as writing `flex: default` and It's the default behavior of all flex items.
Let me break this down, just a bit...

![flex-shorthand](http://i.imgur.com/5DV0ZeR.jpg)

It's easier to understand this by taking a look first at the `flex-basis` property first. It is set to `auto`, which means the initial width of the flex-item will be _automatically_ determined based off the size of the contents. Got that?

Moving on to the next property, the `flex-grow` value being zero also means that the `flex-grow` property wouldn't tamper with the initial width of the flex item. The switch's off.
Since flex-grow controls the "growth" of the flex-items and it's set to zero, the flex-items here wouldn't "grow" to fit the screen.
Finally, the flex shrink value being 1, says this - _"shrink the flex-item when it is necessary"_

Here is what this looks like when applied to our list items:

![flex-shorthand-1](http://i.imgur.com/OVqhSvc.png)

### 2. `Flex: 0 0 auto`

```css
/*again, the 'li' represents any list-item*/

li {
  flex: 0 0 auto;
}
```

This is same as `flex: none`. Using the same framework i established earlier, the width is computed automatically BUT the flex item does NOT grow or shrink (they are both set to zero). It's essentially a fixed width element whose initial width is based off of the content size in the item.

![flex-shorthand-2](http://i.imgur.com/MYYrQia.png)

It doesn't look like anything's changed, right?
Try resizing your browser, and you'll notice that the flex items do NOT shrink even if they pop out of the parent element (we will deal with this later). You'd have to scroll your browser horizontally to view all the content.

![flex-shorthand](http://i.imgur.com/JYZl3GJ.png)

### 3. `Flex: 1 1 auto`

This is same as `flex: auto`. Using the same approach you've used so far, this says, "compute initial width automatically, but grow to fit the entire available space and shrink if necessary"

![flex shorthand 3](http://i.imgur.com/XPKnjC7.png)

This time around the items fill up the available space and they shrink upon resizing the browser.

### 4. `Flex: "positive number"`

Where "positive number" represents any positive number (without the quotes)
This is the same as flex: "positive number" 1 0. For example, `flex:2` is the same as `flex: 2 1 0` where 2 represents any positive number.

```css
/*again, the 'li' represents any list-item*/
li {
  flex: 2 1 0; /*same as flex: 2*/
}
```

Following the same framework I established earlier, this translates to: set the initial width of the flex item to zero (ehm, no width?), grow the item to fill the available space, and finally shrink the item whenever possible (you'd easily notice this when you resize your browser).

It's more practical to use this when you have more than one flex items whose initial widths, `flex-basis` are set to 0% (or any other zero based values e.g. 0px). What really happens is, the widths of the flex items are computed based on the ratios of the `flex-grow` value. I'd break that down just a bit.

Consider two list items (being our flex-items here) marked up and styled below.

```html
<ul>
	<li>I am One</li>
	<li>I am Two</li>
</ul>
```

```css
ul {
  display: flex;
}
li:nth-child(1) {
  flex: 2 1 0; /*same as just writing flex: 2*/
}

li:nth-child(2) {
  flex: 1 1 0;
  background-color: #8cacea;
}
```

Remember that setting `flex-grow : 1` lets the flex-item fill up the available space. Here you have two flex-items. One has a `flex-grow` property of `1` and the other `2`, what then happens?
They both expand to fill up the available space, but in some proportion. Here's how it works.

The latter takes up 2/3 of the available space while the former takes 1/3. You know how I arrived at that? Basic mathematics ratio. `individual ratio / total ratio`

![flex-shorthand 4](http://i.imgur.com/5bslNpH.png)

You see what's happening? Even though both flex-items have contents of the same size (approximately), they however take up different space with one being two times the other.

### 5. Align-self

The `align-self` property takes a step further in giving us so much control. You already saw how the `align-items` property helped in collectively aligning all flex-items within a flex-container. So, what if you wanted to change the position of a single flex-item along the cross-axis, without affecting the neighbouring flex-items?
The `align-self` property comes to the rescue. It may take on any of these values: `auto || flex-start || flex-end || center || baseline || stretch`

```css
li:first-of-type {
  align-self: auto || flex-start || flex-end || center || baseline || stretch;
}
```

These are values you're already similar with, but as a refresher here's how they affect a particular targeted item. In this case, the first item within the container.

### `flex-end`

![flex-end](http://i.imgur.com/1sdtEvg.png)

### `center`

![center](http://i.imgur.com/20l9Vno.png)

### `stretch`

![stretch](http://i.imgur.com/fZZsL2y.png)

### `baseline`

![baseline](http://i.imgur.com/he9J3iB.png)

### `auto`

![auto](http://i.imgur.com/2ZVbkIe.png)

And this is the base styling on the elements, just so you understand what's going on even better.

```css
ul {
  display: flex;
  border: 1px solid red;
  padding: 0;
  list-style: none;
  justify-content: space-between;
  align-items: flex-start; /*affects all flex-items*/
  min-height: 50%;
  background-color: #e8e8e9;
}

li {
  width: 100px;
  background-color: #8cacea;
  margin: 8px;
  font-size: 2rem;
}
```

You're pretty much getting ready for the fun part now :-)

---
