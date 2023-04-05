### ***Integrating PIR Sensor with Arduino***

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/107066424/230141607-934f0b7d-784d-446f-8b7b-751ce7a7d128.png" width="650">

<hr>

***Arduino Code***

```cpp

int sensorState = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);

}

void loop()
{
  sensorState = digitalRead(2);
  if (sensorState == HIGH) {
    digitalWrite(LED_BUILTIN, HIGH);
    Serial.println("Sensor activated!");
  } else {
    digitalWrite(LED_BUILTIN, LOW);
  }
  delay(10); 
}

```
