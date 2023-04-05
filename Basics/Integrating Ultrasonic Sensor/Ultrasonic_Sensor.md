### ***Integrating Ultrasonic Sensor using Arduino***

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
