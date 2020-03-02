---
title: "DOM Navigation Simplified"
description: "DOM allows us to do anything with elements and their contents, but first we need to reach the corresponding DOM object. All operations on…"
date: "2020-03-02T06:47:40.936Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/dom-navigation-simplified-ecdaebe18cd8
redirect_from:
  - /dom-navigation-simplified-ecdaebe18cd8
---

DOM allows us to do anything with elements and their contents, but first we need to reach the corresponding DOM object. All operations on the DOM start with the `document` object. From it we can access any node.

The topmost tree nodes are available directly as `document` properties:

`<html>` = `document.documentElement`

The topmost document node is `document.documentElement`. That’s the DOM node of the `<html>` tag.

`<body>` = `document.body`

Another widely used DOM node is the `<body>` element – `document.body`.

`<head>` = `document.head`

The `<head>` tag is available as `document.head`.

There are two terms that we’ll use from now on:

-   **Child nodes (or children)** — elements that are direct children. In other words, they are nested exactly in the given one. For instance, `<head>` and `<body>` are children of `<html>` element.
-   **Descendants** — all elements that are nested in the given one, including children, their children and so on.

Properties `firstChild` and `lastChild` give fast access to the first and last children.

They are just short-hands. If there exist child nodes, then the following is always true:

```js
elem.childNodes[0] === elem.firstChild
elem.childNodes[elem.childNodes.length - 1] === elem.lastChild
```

There’s also a special function `elem.hasChildNodes()` to check whether there are any child nodes.

As we can see, `childNodes` looks like an array. But actually it’s not an array, but rather a _collection_ – a special array-like iterable object.

There are two important consequences:

We can use `for..of`to iterate over it:

```js
for (let node of document.body.childNodes) {
  alert(node); 
}
```

That’s because it’s iterable (provides the `Symbol.iterator` property, as required).

Array methods won’t work, because it’s not an array:

```js
alert(document.body.childNodes.filter); 
```

If we want to use Array methods

```js
alert( Array.from(document.body.childNodes).filter ); 
```

_Siblings_ are nodes that are children of the same parent.

For instance, here `<head>` and `<body>` are siblings:

```HTML
<html>
  <head>...</head><body>...</body>
</html>
```

-   `<body>` is said to be the “next” or “right” sibling of `<head>`,
-   `<head>` is said to be the “previous” or “left” sibling of `<body>`.

The next sibling is in `nextSibling` property, and the previous one – in `previousSibling`.

The parent is available as `parentNode`.

Navigation properties listed above refer to _all_ nodes. For instance, in `childNodes` we can see both text nodes, element nodes, and even comment nodes if there exist.

But for many tasks we don’t want text or comment nodes. We want to manipulate element nodes that represent tags and form the structure of the page.

The links are similar to those given above, just with `Element` word inside:

-   `children` – only those children that are element nodes.
-   `firstElementChild`, `lastElementChild` – first and last element children.
-   `previousElementSibling`, `nextElementSibling` – neighbor elements.
-   `parentElement` – parent element.
