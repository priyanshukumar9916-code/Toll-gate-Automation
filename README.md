Automatic Toll Gate Using Ultrasonic Sensor & Servo Motor

This project demonstrates an automatic toll gate system using an HC-SR04 ultrasonic sensor and a servo motor controlled by an Arduino.
When an object or vehicle comes within 30 cm, the servo rotates to open the gate, and closes automatically when the object moves away.

📌 Components Required

Arduino Uno / Nano

HC-SR04 Ultrasonic Sensor

SG90/MG995 Servo Motor

Jumper Wires

External power supply (optional for servo)

📌 Circuit Connections
Ultrasonic Sensor (HC-SR04)
Sensor Pin	Arduino Pin
VCC	5V
GND	GND
TRIG	2
ECHO	3
Servo Motor
Servo Wire	Arduino Pin
Signal	4
VCC	5V
GND	GND
📌 Code Explanation

Ultrasonic sensor measures distance using pulse echoes.

If object is closer than 30 cm, servo rotates to 90° (gate opens).

Otherwise, servo stays at 0° (gate closed).

Distance is displayed on the Serial Monitor.

📌 Arduino Code
// Eazytronic.com
#include <Servo.h> // servo library

Servo s1;
const int trigPin = 2;
const int echoPin = 3;

long duration;
int distanceCm, distanceInch;


📌 How It Works

Ultrasonic sensor continuously checks distance.

When a vehicle approaches (less than 30 cm), the servo rotates to open the toll gate.

After the vehicle passes, gate closes automatically.

📌 Notes

If the servo vibrates, use an external 5V supply for stable power.

Increase delay if gate needs to stay open longer.

Can be expanded with RFID, display, or payment simulation.
