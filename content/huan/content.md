# Chapter Title

## First Section

> sectionId: section-1
> id: step-1

Here is a paragraph

There are numbers like [[10]] or [[ten]] and [[many|few|no]] choices.

---
> sectionId: section-2
> id: step-2

Here is another paragraph

Here is a code editor. Type “I love Mathigon” anywhere in the text box to
proceed:

The square of ${a}{a|1|-4,4,1} is ${a*a}.


--------------------------------------------------------------------------------

## 介绍

> section: introduction
> id: intro

::: column.grow

For as long as humans exist, we have looked to the sky and tried to explain life
on Earth using the motion of stars, planets and the moon.

Ancient Greek astronomers were the first to discover that all celestial objects
move on regular paths, called __orbits__. They believed that these orbits are
always circular. After all, circles are the “most perfect” of all shapes:
symmetric in every direction, and thus a fitting choice for the underlying
order of our universe.

::: column(width=320)

    x-media(src="images/geocentric.jpg" width=320 height=272)

{.caption} Earth is at the center of the _Ptolemaic universe_.

:::

---
> id: radius
> goals: compass

Every point on a [__circle__](gloss:circle) has the same distance from its
center. This means that they can be drawn using a [compass](gloss:compass):

::: column(width=320)

    x-geopad(width=320 height=300 style="position: relative;")
      svg(style="stroke-linecap: round; stroke-linejoin: round")
        circle.move(name="a" cx=160 cy=150 target="r d")
        circle.move.reveal(name="b" cx=250 cy=240 project="circle(a, 120)" target="r" when="compass")
        path.red(x="segment(a,b).contract(0.08)" target="r" arrows="both" hidden)
        path(name="c1" x="arc(a,b,1.99*pi)" hidden)
        path.blue(x="segment(b.rotate(Math.PI/3,a),b.rotate(-2*Math.PI/3,a)).contract(0.01)" target="d" arrows="both" hidden)
        path.green(x="arc(a,b.add(b.subtract(a).normal.scale(12)),1.99*pi).contract(0.02)" target="c" arrows="start" hidden)
      x-play-btn

::: column.grow

{.reveal(when="compass")} There are three important measurements related to
circles that you need to know:

* {.reveal(when="compass" delay="1000")} The [{.step-target.pill.b.red}radius](target:r)
  is the distance from the center of a circle to its outer rim.
* {.reveal(when="compass" delay="4000")} The [{.step-target.pill.b.blue}diameter](target:d)
  is the distance between two opposite points on a circle. It goes through its
  center, and its length is [[twice|half|the same as]] the radius.
* {.reveal(when="blank-0")} The [{.step-target.pill.b.green}circumference](target:c) 
  (or perimeter) is the distance around a circle.

:::

---