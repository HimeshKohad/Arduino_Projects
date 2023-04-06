### ***LED Blinker Circuit using Arduino***

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
  digitalWrite(LED_BUILTIN, HIGH);
  delay(500); // Wait for 500 millisecond(s)
  digitalWrite(LED_BUILTIN, LOW);
  delay(500); // Wait for 500 millisecond(s)
}

```
