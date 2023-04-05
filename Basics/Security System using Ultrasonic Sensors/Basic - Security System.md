### ***Basic - Security System using Ultrasonic Sensor***

<hr>

***Circuit Diagram***

<img src="https://user-images.githubusercontent.com/107066424/230139683-1a2add51-8c75-42b7-84bb-b72064a65196.png" width="650">

<hr>

***Arduino Code:***

```cpp

int input = 0;

long readUltrasonicDistance(int triggerPin, int echoPin) {
  pinMode(triggerPin, OUTPUT);  // Clear the trigger
  digitalWrite(triggerPin, LOW);
  delayMicroseconds(2);
  
  // Sets the trigger pin to HIGH state for 10 microseconds
  digitalWrite(triggerPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(triggerPin, LOW);
  pinMode(echoPin, INPUT);
  
  // Reads the echo pin, and returns the sound wave travel time in microseconds
  return pulseIn(echoPin, HIGH);
}

void setup() {
  Serial.begin(9600);

  pinMode(8, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
}

void loop()
{
  input = 0.01723 * readUltrasonicDistance(6, 5);
  Serial.println(input);
  
  if (input <= 100) {
    digitalWrite(8, HIGH);
    digitalWrite(9, HIGH);
    digitalWrite(10, LOW);
  } 
  
  else {
    digitalWrite(8, LOW);
    digitalWrite(9, LOW);
    digitalWrite(10, HIGH);
  }
  
  delay(10); // Add a small delay to improve performance while simulating
}

```
