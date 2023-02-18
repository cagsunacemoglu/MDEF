# Design Tools (2D, 3D, Parametric Design)

As someone with a background in electronics engineering and experience design, this class has been an eye-opening experience for me. In both of these fields, the things that are designed always result in physical artifacts. However, in the past, these were created by others, so being able to design physical objects myself is very intriguing.

I enjoyed learning about the modern possibilities, although I found it almost overwhelming to see the technological advances nowadays. With parametric design, generative technologies, and the utilization of AI, the tool and software landscape in this field is incredibly advanced and varied, which is mind-blowing.

## Exercise 1 - Parametric Modelling of a Croissant 

In Exercise 1, which involved parametric modeling of a croissant, I quickly sketched a rough design on paper using my non-existent drawing skills. The idea is (from top view) that there are two intersecting curves, with several cuts across the surface between them. The distance between the cuts and the radius of those section determine the rough shape of the croissant.

![](https://i.imgur.com/Fmg8LkT.jpg)


The reality is much more complex of course, and this made me recognise that even a simple everyday object like a croissant is such a complicated design at the moment of creation. 
The other takeaway for me was that sometimes it’s much easier to design things with our hands: You can shape a croissant from dough but designing that on a software is rather difficult. Conversely, designing a perfect sphere is almost impossible by hand, but it can be done with a few clicks in software.

In Exercise 2 - Algorithmic Design 

In one of my interventions, we’re working on an indoor modular water wall made out of water bricks, so I decided to work with a rectangle prism that could be the basis of such a brick to experiment with parametric design.

I had no previous experience with parametric design, so this was basically an exploration on how the basics work. It wasn’t as straight forward I thought it would be, and it took me a while to be able to draw a rectangle, and then convert that to a rectangle prism parametrically. (It was also surprising to me that it’s not possible to draw something directly in Rhino and press a button that transforms it into a parametric version.)

So I started from scratch and build a parametric system step by step.
First step was to define the points that make up the rectangle. 

First I started with static points that defined a rectangle by adding a Rect2Pt  object and define 2 points manually. The panel was showing that a rectangle was created although it’s not visible on screen.

![](https://i.imgur.com/YzDwfmn.png)

Then I added a BoxRec object with variable height that can be adjusted by a slider. By doing this, the height of the prism was parametrised.

![](https://i.imgur.com/9ERYlrn.gif)


Finally I turned point B of the rectangle into coordinate parameters which allowed me to create a box with variable size through 4 parameters: Starting point, coordinates x & y of second corner of the base rectangle and the height of the prism.

![](https://i.imgur.com/XKgl7b2.gif)
