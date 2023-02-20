# Inputs & Outputs

This class was quite an exhaustive coverage of types of sensors, how they work and their potential applications. Having worked with sensors before, I enjoyed going through such a complete list and discussing them in detail.

I also reflected on the fact that, when I studied electronics engineering, we didn’t have a class on sensors specifically, and I recognised how much it was actually needed. This is an important topic that has its own intricacies and shouldn’t be taken for granted otherwise working with sensors can become very cumbersome without the base technical knowledge.

The exercise for the class was to: “Use a sensor and an actuator to communicate”, and the guidance was to use a Light Dependant Resistor (LDR) to detect the light level and pair our LDR with a LED which we can then control to transfer information to the LDR optically, in order to build something like an optic Telegraph.

I utilised some great resources to follow the exercise. 
Following [Using a Photocell | Photocells | Adafruit Learning System](https://learn.adafruit.com/photocells/using-a-photocell), and using the same circuitry and code I was able to get my LDR to sense dim vs. bright light.

![](https://i.imgur.com/vVHTxsQ.gif)

Then following  [Arduino - Turn LED ON and OFF With Button - The Robotics Back-End (roboticsbackend.com)](https://roboticsbackend.com/arduino-turn-led-on-and-off-with-button/)  I was able to turn Led on and off using another Arduino board I had available. 

![](https://i.imgur.com/llUTbyn.gif)

This way I was able to run both devices at the same time without integrating their circuits & code.

![](https://i.imgur.com/IVyqQYd.gif)

I tried to use an optic cable that came with the modem to transfer the information between the boards, but it didn’t work. The light from the end of the cable wasn’t visible to eye, so it was no surprise that LDR didn’t catch it. 

Then I went forward as the exercise suggested, and tried to recognise dots and dashes following this tutorial, but I couldn’t make it work as I haven’t been able to figure out how to detect the length of the light pulse yet.
[Arduino Morse Decoder](http://persion.info/projects/arduino-morse-decoder/) 