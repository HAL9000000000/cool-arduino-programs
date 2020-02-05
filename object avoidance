/*
   object avoidance. Drives forward until object
  detected at 10 cm than turns randomly left or
  right. pin 13 left motor forwards. pin 12 left
    motor back. pin 11 right motor forwards. pin
  10 right motor back
*/

int inches = 0;

int cm = 0;

int turn = 0;

long readUltrasonicDistance(int triggerPin, int echoPin)
{
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

void setup()
{
  pinMode(13, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(10, OUTPUT);
}

void loop()
{
  while (1 < 2) {
    while (0.01723 * readUltrasonicDistance(2, 2) > 15) {
      digitalWrite(13, HIGH);
      digitalWrite(11, HIGH);
      // drive forwards
    }
    if (0.01723 * readUltrasonicDistance(2, 2) < 15) {
      turn = random(1, 10 + 1);
    }
    if (turn < 5) {
      digitalWrite(12, HIGH);
      digitalWrite(11, HIGH);
      // turn left
    } else {
      digitalWrite(13, HIGH);
      digitalWrite(10, HIGH);
      // turn right
    }
  }
}
