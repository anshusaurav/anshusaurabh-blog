---
title: "Alignment in Flexible Box Model"
description: "If you have ever been confused about when to align and when to justify, I hope this article will make things clearer!"
date: "2020-02-05T05:13:53.162Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/alignment-in-flexible-box-model-3bc1cf9cae27
redirect_from:
  - /alignment-in-flexible-box-model-3bc1cf9cae27
---

If you have ever been confused about when to align and when to justify, I hope this article will make things clearer!

Many people tell me that they struggle to remember whether to use properties which start with align- or those which start with justify- in flexbox. The thing to remember is that:

justify- performs main axis alignment. Alignment in the same direction as your flex-direction

align- performs cross-axis alignment. Alignment across the direction defined by flex-direction. Thinking in terms of main axis and cross axis, rather than horizontal and vertical really helps here.

**MAIN AXIS ALIGNMENT WITH**

**Justify-Content**

We will start with the main axis alignment. On the main axis, we align using the justify-content property. This property deals with all of our flex items as a group, and controls how space is distributed between them.

**1.Flex-Start:** The initial value of justify-content is flex-start. This is why, when you declare display: flex all your flex items line up against the start of the flex line. If you have a flex-direction of row and are in a left to right language such as English, then the items will start on the left.

![Justify-content: Flex-start](./asset-1)

Note that the justify-content property can only do something if there is spare space to distribute. Therefore if you have a set of flex items which take up all of the space on the main axis, using justify-content will not change anything.

![Justify-content is still Flex-start but elements take all the available space.](./asset-2)

**2\. Flex-End:** If we give justify-content a value of flex-end then all of the items will move to the end of the line. The spare space is now placed at the beginning.

![Justify-content:Flex-end](./asset-3)

**3\. Space-Between:** We can do other things with that space. We could ask for it to be distributed between our flex items, by using justify-content: space-between. In this case, the first and last item will be flush with the ends of the container and all of the space shared equally between the items.

![Justify-content:space-between](./asset-4)

**4\. Space-around:** We can ask that the space to be distributed around our flex items, using justify-content: space-around. In this case, the available space is shared out and placed on each side of the item.

![Justify-content:space-around](./asset-5)

**5\. Space-evenly:** A newer value of justify-content can be found in the Box Alignment specification; it doesn’t appear in the Flexbox spec. This value is space-evenly. In this case, the items will be evenly distributed in the container, and the extra space will be shared out between and either side of the items.

![Justify-content:space-evenly](./asset-6)
