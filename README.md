# IoT-Smart-Lock-Using-ESP32-and-Touch-Sensors
📌 Connection Configuration
Microcontroller: ESP32 Dev Board
We'll use GPIO pins (customizable if needed).

🔘 Touch Sensors (TTP223)
Sensor	Pin	Connected to ESP32 GPIO
A	OUT	D32 (Touch Sensor 1)
B	OUT	D33 (Touch Sensor 2)
C	OUT	D25 (Touch Sensor 3)
D	OUT	D26 (Touch Sensor 4)
E	OUT	D27 (Touch Sensor 5)

⚡ VCC of all sensors → 3.3V (ESP32)
🧲 GND of all sensors → GND (ESP32)

🔌 Relay Module (1-Channel)
Relay Pin	Connect to
VCC	3.3V or 5V (ESP32)
GND	GND (ESP32)
IN	D4 (ESP32)

🔄 This pin is HIGH/LOW to trigger the relay

🔐 Solenoid Lock
Wire (Color)	Connect to
Red (+)	Relay COM
Black (-)	Power Supply GND
Relay NO	+ve Battery Supply

🔋 Use 12V or 7.4V 18650 battery pack (based on your lock voltage)

🔴🟢🔵 LED Indicators
LED Color	Anode (+) → GPIO	Cathode (–) → GND via 220Ω
Green	D16	GND
Blue	D17	GND(RED light recommended)

🔋 Power Supply
ESP32: Via micro USB (or from battery with 5V regulator)

Relay & Lock: Powered via battery pack (3x 18650)

Connect GNDs together (ESP32 and battery must share common ground)

🗂️ Optional Summary Table
Module	ESP32 GPIO	Notes
Touch Sensor A	D32	First digit
Touch Sensor B	D33	Second digit
Touch Sensor C	D25	Third digit
Touch Sensor D	D26	Fourth digit
Touch Sensor E	D27	Fifth digit (or reset)
Relay IN	D4	Controls lock
Green LED	D16	Success feedback
Red LED	D17	Error feedback
Blue LED	D5	System status (optional)
