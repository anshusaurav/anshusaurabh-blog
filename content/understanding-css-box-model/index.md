---
title: "Understanding CSS Box Model"
description: "CSS box model is a container which contains multiple properties including borders, margin, padding and the content itself. It is used to…"
date: "2020-01-28T04:22:42.586Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/understanding-css-box-model-5841a1958373
redirect_from:
  - /understanding-css-box-model-5841a1958373
---

CSS box model is a container which contains multiple properties including borders, margin, padding and the content itself. It is used to create the design and layout of web pages. It can be used as a toolkit for customizing the layout of different elements. The web browser renders every element as a rectangular box according to the CSS box model.  
Box-Model has multiple properties in CSS. Some of them are given below:

-   Borders
-   Margins
-   Padding
-   Content

Border Area: It is the area between the box’s padding and margin. Its dimensions are given by the width and height of border.

Margin Area: This area consists of space between border and margin. The dimensions of Margin area are the margin-box width and the margin-box height. It is useful to separate the element from its neighbors.

Padding Area: It includes the element’s padding. This area is actually the space around the content area and within the border box. Its dimensions are given by the width of the padding-box and the height of the padding-box.

Content Area: This area consists of content like text, image, or other media content. It is bounded by the content edge and its dimensions are given by content box width and height.

The “CSS box model“ is a set of rules that define how every web page on the Internet is rendered. CSS treats each element in your HTML document as a “box” with a bunch of different properties that determine where it appears on the page. So far, all of our web pages have just been a bunch of elements rendered one after another. The box model is our toolkit for customizing this default layout scheme.

A big part of your job as a web developer will be to apply rules from the CSS box model to turn a design mockup into a web page. As you work through this chapter, you might find yourself wondering why we have to learn all these rules instead of just uploading a giant static image of a web page (i.e., a mockup) to a web server and calling it a day.

Indeed, this would make life a lot easier; however, if we didn’t separate out our content into HTML, search engines would have no way to infer the structure of our web pages, we couldn’t make our site responsive, and there would be no way to add fancy animations or interactivity with JavaScript. That’s a big enough trade-off to make CSS a worthwhile cause.

The width and height properties only define the size of a box’s content. Its padding and border are both added on top of whatever explicit dimensions you set. This explains why you’ll get an image that’s 244 pixels wide when you take a screenshot of our button, despite the fact that it has a width: 200px declaration attached to it. Needless to say, this can be a little counterintuitive when you’re trying to lay out a page. Imagine trying to fill a 600px container with three boxes that are all width: 200px, but they don’t fit because they all have a 1px border (making their actual width 202px).
