---
title: "Responsive Web Design"
description: "In current scenario all clients need the application or website to run on multiple sized devices. With recent innovations in mobile…"
date: "2020-03-02T08:23:59.549Z"
categories: []
published: true
canonical_link: https://medium.com/@anshu.saurav/responsive-web-design-33ae03410775
redirect_from:
  - /responsive-web-design-33ae03410775
---

In current scenario all clients need the application or website to run on multiple sized devices. With recent innovations in mobile devices we are forced to build a website which can run on multiple platforms i.e. I-phone, I-pad, Kindle, Android phones, Tablets and a lot of other differently sized devices. In the next five years, we’ll likely need to design for a number of additional inventions. In the field of Web design and development, we’re quickly getting to the point of being unable to keep up with the endless new resolutions and devices.

There are few practices which are common while scaling our website for small sized devices. The practice consists of a mix of flexible grids and layouts, images and an intelligent use of CSS media queries. As the user switches from their laptop to iPad, the website should automatically switch to accommodate for resolution, image size and scripting abilities. In other words, the website should have the technology to automatically respond to the user’s preferences. This would eliminate the need for a different design and development phase for each new gadget on the market.

Responsive design refers to the idea that your website should display equally well in everything from widescreen monitors to mobile phones. It’s an approach to web design and development that eliminates the distinction between the mobile-friendly version of your website and its desktop counterpart. With responsive design, they’re the same thing.

Responsive design is accomplished through CSS media queries. We can think of media queries as a way to conditionally apply CSS rules. They tell the browser that it should ignore or apply certain rules depending on the user’s device.  
Responsive web design patterns are quickly evolving, but there are a handful of established patterns that work well across the desktop and mobile devices.

Patterns — Most of the time we can solve this issue using some of general patterns developed in last few years.

**Mostly Fluid** — The mostly fluid pattern consists primarily of a fluid grid. On large or medium screens, it usually remains the same size, simply adjusting the margins on wider screens.

On smaller screens, the fluid grid causes the main content to reflow, while columns are stacked vertically. One major advantage of this pattern is that it usually only requires one breakpoint between small screens and large screens.

**Column Drop **— For full-width multi-column layouts, column drop simply stacks the columns vertically as the window width becomes too narrow for the content.

Eventually this results in all of the columns being stacked vertically. Choosing breakpoints for this layout pattern is dependent on the content and changes for each design.

**Layout Shifter** — The layout shifter pattern is the most responsive pattern, with multiple breakpoints across several screen widths.

Key to this layout is the way content moves about, instead of re-flowing and dropping below other columns. Due to the significant differences between each major break-point, it is more complex to maintain and likely involves changes within elements, not just overall content layout.

**Tiny Tweaks** — Tiny tweaks simply makes small changes to the layout, such as adjusting font size, resizing images, or moving content around in very minor ways.

It works well on single column layouts such as one page linear websites and text-heavy articles.

**Off Canvas** — Rather than stacking content vertically, the off canvas pattern places less frequently used content — perhaps navigation or app menus — off screen, only showing it when the screen size is large enough, and on smaller screens, content is only a click away.

Now you know the techniques we can use to make a page responsive. The whole process mostly depends on the altercations in user interface to make it accessible to users of different devices. You can try to make your already done projects using above techniques.
