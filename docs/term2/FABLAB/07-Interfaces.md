Interfaces: Machine interactions

We spent the class going through various interesting exercises of lighting up a LED.
I think it was as a great flow of exercises, because LEDs are fun to play with, they’re simple to work with but visually appealing and allow for creativity. The step by step approach was also really nice to build up as we go, and at the end we ended up creating something quite cool, a central server lighting up the LEDs of the whole class through inputs from anyone in the class. 

The highlights for me were
- Discovering about the [jLED animation library](https://https://github.com/jandelgado/jled#usage): I wouldn’t guess there’d be a library for seemingly simple functions like LED lighting, but now I’d think about checking out existing libraries before creating something new
- Learning about node-red and how it works in high-level. It was also good to  learn about  in conjunction with MCCT, although I’d need some time to work with these tools, to understand exactly how they work and what their capabilities are. 
- The ease of creating a connection with a server with a few lines of code, and communicating over wifi through an Arduino device is mind blowing. I hope I get the chance to work with this capability in my design challenges & interventions. 

Here’re some references to materials we used in the class:
* Course material: https://hackmd.io/95FEOJXeSXe9hDu289X-bw?view 
* Node Red: https://nodered.org/
* MQTT Broker: https://mosquitto.org/
* My code to diversify the responses based on incoming messages

```
#include "Arduino.h"
#define LED_PIN 14

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(9600);
}

void blink () {
  digitalWrite(LED_PIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_PIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
void blinkFast () {
  int i=0;
  while(i<20){
    digitalWrite(LED_PIN, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(100);                       // wait for a second
    digitalWrite(LED_PIN, LOW);    // turn the LED off by making the voltage LOW
    delay(100);
    i++;    
  }                       // wait for a second
}
void blinkX (int reps) {
  int i=0;
  while(i<reps){
    digitalWrite(LED_PIN, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(100);                       // wait for a second
    digitalWrite(LED_PIN, LOW);    // turn the LED off by making the voltage LOW
    delay(100);
    i++;
  }                       // wait for a second
}

// the loop function runs over and over again forever
void loop() {

  if (Serial.available()) {
    String newMsg = Serial.readString();
    newMsg.trim();

    Serial.print("Got new message!: ");
    Serial.println(newMsg);

    // blink if we tell it to!
    if (newMsg.equals("a")){
      blink();
    }
    if (newMsg.equals("c")){
      blink();
      blink();
      blink();
    }
    if (newMsg.equals("b")){
      blink();
      blink();
    }
    if (newMsg.equals("fast")){
      blinkFast();
    }
    if (newMsg.equals("b5")){
      blinkX(5);
    }
    if (newMsg.equals("b50")){
      blinkX(50);
    }
  }
}
```


Here is the final video of the collective lighting up of multiple LEDs via the server, via an online interface that can be controlled by anyone in the class. Oscar had shown us a video of a dance show with coordinated and synchronized LED masks at the beginning of the course. We achieved the core functionality of this show (synchronous control of multiple devices over a local network) within 3-4 hours, which is a mind-blowing result that shows the accessibility level of today's technology.

![](https://i.imgur.com/cHTQ513.gif)


