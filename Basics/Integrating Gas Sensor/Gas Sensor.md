### ***Integrating Gas Sensor using Ardino***

<hr>

***Circuit Diagram***

![image](https://user-images.githubusercontent.com/80636388/230439964-15a8d478-56e9-4c4e-b836-bada207fec92.png)

<hr>

***Arduino Code***

```cpp

int gassensor = 0;

void setup()
{
  pinMode(A5, INPUT);
  Serial.begin(9600);
  pinMode(2, OUTPUT);
}

void loop()
{
  gassensor = analogRead(A5);
  Serial.println(gassensor);
  if (gassensor > 200) {
    tone(2, 523, 1000); // play tone 60 (C5 = 523 Hz)
  }
  delay(10); // Delay a little bit to improve simulation performance
}

```
