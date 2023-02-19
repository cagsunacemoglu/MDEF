# Micro Challenge 1
As we were a team of people interested in working with water in the domestic space, we chose to work on a water quality measurement system that could be useful to assess water as part of a filtration or cultivation system.

We researched that to assess the quality of water, a number of sensors were required. We decided to go for pH and EC (electro conductivity -  an indicator of the amount of solids in water sensors) and temperature (to make sense of EC which is dependent on the temperature of water) which were available in Fablab. 

After deciding on these, it was possible to break the project down into smaller pieces of work and attack them by smaller teams. While some of us worked on the physical design of the unit, I worked on electronics:  Making the EC sensor work, integrating a pump to flow the water that will be measured and bringing together the system.

![](https://i.imgur.com/i4chBPB.jpg)

> `All code and other documentation is in the project repo at the end of the page.`

## Using Parrot as an EC Sensor

It turned out to be a technically complicated challenge: The EC sensor we chose to use was an off-the-shelf product called Parrot, due to being abundantly available in Fablab. To make it work, we had to use an open source library that was written in Node; thus we had to use a Raspberry Pi that could run Node code. 

[GitHub - sandeepmistry/node-flower-power: node.js lib for the Parrot Flower Power](https://github.com/sandeepmistry/node-flower-power)

It took me and Mikel  more than a day to make the base installations to be able run the open source library without errors, and get some readings from the EC sensor. Then I simplified the code to only get the EC, and temperature data we need. 

![](https://i.imgur.com/RTjPqXM.jpg)


## Integrating a Pump
Integrating a pump was rather easy, I found a simple resource that explains how to run a motor through a MOSFET, that ran smoothly in the first try.
[Transistor Motor Control | Arduino Documentation | Arduino Documentation](https://docs.arduino.cc/learn/electronics/transistor-motor-control)

## Integrating the Electronic System
So, we had a system that consisted of
- a Raspberry Pi that talks to the EC sensor (Parrot)
- an Arduino that talks to the Ph sensor and runs the pump

I established serial communication between the Raspberry Pi and Arduino, such that Arduino acts like a sensor that transmits Ph reading continuously until a button is pressed.
 When someone presses the button, Arduino runs the pump and an EC measurement is done.
 
![](https://i.imgur.com/fpaTgVu.jpg)

![](https://i.imgur.com/x4kSVkv.png)

![](https://i.imgur.com/tK2qoZD.jpg)

![](https://i.imgur.com/tgWHuVJ.png)


## Reflection
There have been positive personal and team learnings from the project:
It was an accelerated learning experience for me to work with Raspberry Pi, which I have not been exposed to before. On the team level, I think working on a water-tight unit that we can programmatically pump water into was very nice. The sensors need more work for calibration and making sense, we are getting some readings which look accurate, but we don’t know what it tells us in terms of water quality.

Overall, I think the project quickly turned into an engineering challenge, maybe too deep for the purpose of this micro challenge. In the next challenges I’d prefer to go less technical, and focus on something that generates more meaningful results in the human scale, possibly through using some of the learnings from this challenge.

## Project Repo:

Scripts and other documentation is in the project repo below.
[GitHub - ramiroarga/WATER: Water explorations for Microchallenges](https://github.com/ramiroarga/WATER)