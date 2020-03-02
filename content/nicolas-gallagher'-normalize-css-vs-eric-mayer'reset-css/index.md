---
title: "Nicolas Gallagher’ Normalize CSS vs Eric Mayer’Reset CSS"
description: "All web browsers add their own style formatting to HTML elements for a more readable document. But not all browsers treat HTML in the same…"
date: "2020-01-22T15:36:01.444Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/nicolas-gallagher-normalize-css-vs-eric-mayer-reset-css-458a31b048b4
redirect_from:
  - /nicolas-gallagher-normalize-css-vs-eric-mayer-reset-css-458a31b048b4
---

All web browsers add their own style formatting to HTML elements for a more readable document. But not all browsers treat HTML in the same way. For example, _Safari_ and _Chrome_ will display the same HTML document differently, and these differences are due to built-in browser styling.we want an HTML elements to look the same way, independent of which browser is being used to view it. Unfortunately, this is not the case because of the way browsers run. Historically web developers used to use CSS files called resets, which removed all the default browser styling applied to HTML, and then applied their own styles for everything over the top — this was done to make styling on a project more consistent, and reduce possible cross browser issues, especially for things like layout.

![CSS Reset](./asset-1.jpeg)

As you can see in reset.css we see all headings i.e. `h1,h2,h3….h6` are trimmed down to same size whereas in normalize.css modifies only `h1` and don’t disturb other headings.

![Normalize CSS](./asset-2.jpeg)

Results we obtain by using `reset.css` are as follows for all headings.

![Results obtained on chrome for heading h1,h2,h3,h4,h5 and h6 by reset.css](./asset-3.jpeg)

Similarly, when we use `normalize.css`, we get following results:

![Results obtained on chrome for heading h1,h2,h3,h4,h5 and h6 by normalize.css](./asset-4.jpeg)

While using both CSS files, result will be dominated by the one which is used later in html file as expected.

So we can see normalize CSS just normalizes the document i.e. not being harsh with the document, In the same place reset CSS trims all style and differences and make look all elements same. `Normalize.css` will fix the browser style that has the difference.

This is only some observation which we can observe using basic html code. Eric Meyer, when he pioneered the technique of CSS Reset, explicitly said that:

“The reset styles given here are intentionally very generic. I don’t particularly recommend that you just use this in its unaltered state in your own projects. **It should be tweaked, edited, extended, and otherwise tuned to match your specific reset baseline.** Fill in your preferred colors for the page, links, and so on. In other words, this is a starting point, not a self-contained black box of no-touchiness.”

So I think we should use both but smartly. We can use the benefits of each of the methods. On the one hand,we can the benefits of the Normalize CSS, while in other cases we want the benefits of a CSS Reset without those big chains of bad looking CSS selectors.
