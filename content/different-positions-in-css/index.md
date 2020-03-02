---
title: "Different Positions in CSS"
description: "The CSS position property defines how the element is positioned on the web page. The CSS position property defines, as the name says, how…"
date: "2020-01-31T04:29:38.656Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/different-positions-in-css-81cd45676b65
redirect_from:
  - /different-positions-in-css-81cd45676b65
---

The CSS position property defines how the element is positioned on the web page. The CSS position property defines, as the name says, how the element is positioned on the web page.

There are several types of positioning: static, relative, absolute, fixed. First of all, let’s explain what all of these types mean.

**Static **— This is the default value, all elements are in order as they appear in the document.  
**Relative** — The element is positioned relative to its normal position.  
**Absolute** — The element is positioned absolutely to its first positioned parent.  
**Fixed** — The element is positioned related to the browser window.

Two most commonly used position values — **relative and absolute**.

**Relative Positioning-** When you set the position relative to an element, without adding any other positioning attributes (top, bottom, right, left) nothing will happen. When you add an additional position, such as left: 20px the element will move 20px to the right from its normal position. Here, you can see that this element is relative to itself. When the element moves, no other element on the layout will be affected. In relative positioning any element that is the child of this element can be absolutely positioned within this block.

**HTML**

```
<div id=”first_element”>First element</div> 
<div id=”second_element”>Second element</div>
```

**CSS**

```
#first_element { 
 position: relative; 
 left: 30px; 
 top: 70px; 
 width: 500px; 
 background-color: #fafafa; 
 border: solid 3px #ff7347; 
 font-size: 24px; 
 text-align: center; 
}

#second_element { 
 position: relative; 
 width: 500px; 
 background-color: #fafafa; 
 border: solid 3px #ff7347; 
 font-size: 24px; 
 text-align: center; 
}
```

In this example, you will see how the relatively positioned element moves when its attributes are changed. The first element moves to the left and top from its normal position, while the second element stays in the same place because none of the additional positioning attributes were changed.

**Relative Positioning**: This type of positioning allows you to place your element precisely where you want it.

The positioning is done relative to the first relatively (or absolutely) positioned parent element. In the case when there is no positioned parent element, it will be positioned related directly to the HTML element (the page itself).

**HTML**

```
<div id=”parent”>
 <div id=”child”></div>
</div>
```

**CSS**

```
#parent { 
 position: relative; 
 width: 500px; 
 height: 400px; 
 background-color: #fafafa; 
 border: solid 3px #9e70ba; 
 font-size: 24px; 
 text-align: center; 
}

#child { 
 position: absolute; 
 right: 40px; 
 top: 100px; 
 width: 200px; 
 height: 200px; 
 background-color: #fafafa; 
 border: solid 3px #78e382; 
 font-size: 24px; 
 text-align: center; 
}
```

In the example, the parent element has the position set to relative. Now, when you set the position of the child element to absolute, any additional positioning will be done relative to the parent element. The child element moves relative to the top of the parent element by `100px`and right of the parent element by `40px`.
