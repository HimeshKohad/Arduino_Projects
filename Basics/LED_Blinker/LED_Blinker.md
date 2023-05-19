### ***LED Blinker Circuit using Arduino***

<hr>

LEDs are small, powerful lights that can be found in a variety of applications. 
To begin, we will practice blinking an LED, which is the Hello World of microcontrollers. It is as simple as turning on and off a light switch. 
Establishing this critical baseline will provide you with a solid foundation as we progress to more complex experiments.

***Components Required:***
- 1 x Breadboard
- 1 x Arduino Uno
- 1 x LED
- 1 x 330 Ω Resistor
- 3 x Jumper Wires

<br>

***Note:*** If you need to figure out the polarity of an LED, look at its terminals carefully. The shorter of the two terminals, towards the flat edge of the bulb indicates _'negative terminal'_.

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/107066424/230366626-904477ba-7252-4347-8ed1-ebe85dee8742.png" width="650">

<hr>

***Arduino Code***

```cpp

void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  digitalWrite(LED_BUILTIN, HIGH); // turn the LED 'ON' by making the voltage HIGH
  delay(1000); // Wait for a second
  digitalWrite(LED_BUILTIN, LOW); // turn the LED 'OFF' by making the voltage LOW
  delay(1000); // Wait for a second
}

```
