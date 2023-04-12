### ***Basic - Security System using PIR Sensor***

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/80636388/231520860-103e85d4-6732-4bce-9074-e70c642a4fdf.png" width="650">

<hr>

***Arduino Code:***

```cpp

int pir_pin = 2;
int led_pin = 3;
int buzzer_pin = 4;
void setup()
{
 pinMode(pir_pin, INPUT);
 pinMode(led_pin, OUTPUT);
 pinMode(buzzer_pin, OUTPUT);
 Serial.begin(9600);
}

void loop()
{
  if(digitalRead(pir_pin) == HIGH)
   {
  	digitalWrite(led_pin, HIGH);
    digitalWrite(buzzer_pin, HIGH);
    Serial.println("Detectado");
   }
   else{
    digitalWrite(led_pin, LOW);
    digitalWrite(buzzer_pin, LOW);
    Serial.println("No Detectado");
   }
}

```
