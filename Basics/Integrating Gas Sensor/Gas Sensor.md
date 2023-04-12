### ***Integrating Gas Sensor using Arduino***

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/80636388/231523319-42024b24-be04-4d36-92fc-9ca0deafd6de.png" width="650">

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
