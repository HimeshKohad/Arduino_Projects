### ***Integrating Ultrasonic Sensor using Arduino***

<hr>

[Ultrasonic sensors](https://github.com/HimeshKohad/Arduino_Projects/blob/main/Workings/Ultrasonic%20Sensor.md) are commonly used in Arduino projects for distance measurement. 
An ultrasonic sensor is a device that uses ultrasonic waves for distance measurement. It works on the principle of sending out ultrasonic pulses and measuring the time it takes for those pulses to bounce back after hitting an object. This time measurement can then be used to calculate the distance between the sensor and the object.
<br>In this project, we'll integrate an ultrasonic sensor with Arduino to measure distances accurately.

_**Components Required:**_

- 1 x Arduino Uno
- 1 x Ultrasonic Sensor
- 1 x Breadboard
- Jumper Wires

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/107066424/230143774-347f17b7-242f-4e30-8c4f-b80ad29667da.png" width="650">

<hr>

***Arduino Code***

```cpp

int trig = 13;
int echo = 12;

float distance;	


void setup()	
{
  pinMode (trig, OUTPUT);
  pinMode (echo,INPUT);
  
  Serial.begin (9600);
}

void loop()
{
  digitalWrite(trig, LOW);
  delay(5);
  digitalWrite(trig, HIGH);
  delay(10);
  digitalWrite(trig, LOW);
  
  distance = pulseIn (echo, HIGH);
  distance = distance/58;
  Serial.println (distance);
}

```
