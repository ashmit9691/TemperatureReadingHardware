🌡️ DHT‑11 IoT Sensor with ESP8266 & Blynk:
A quick project that sends real‑time temperature (°C) and humidity (%) data from a DHT‑11 sensor to the Blynk IoT Cloud using an ESP8266 (NodeMCU).

✨ What it does:

Feature	                               Details
📡 Wi‑Fi Upload	                       ESP8266 reads the sensor every second and publishes the data to Blynk Cloud.
📲 Mobile Dashboard	                   Two Blynk widgets (V0 ✦ temperature, V1 ✦ humidity) update live in the Blynk App or Web dashboard.
🔧 Serial Debug	                       Values are printed to the Serial Monitor for quick troubleshooting.


🛠️ Hardware:
Qty	   Part
1	     ESP8266 development board (NodeMCU / Wemos D1 mini)
1	     DHT‑11 temperature‑&‑humidity sensor
1	     Breadboard + jumper wires
—	     5 V USB power for the ESP

DHT‑11  →  ESP8266
   VCC  →  3.3 V
   GND  →  GND
   DATA →  D2  (GPIO 4)   ← change DHTPIN if you wire differently


💻 Software / Libraries:

Library	Install via Arduino IDE 🔽
Blynk (legacy & v2)
Blynk	Sketch ▸ Include Library ▸ Manage Libraries…
DHT sensor library
DHT sensor library by Adafruit	
Adafruit Unified Sensor
Adafruit Unified Sensor (dependency for DHT)	
ESP8266 core	File ▸ Preferences ▸ Boards Manager URL
http://arduino.esp8266.com/stable/package_esp8266com_index.json → install “esp8266” via Boards Manager

![image](https://github.com/user-attachments/assets/de458c47-3328-4c5f-834d-a9bcad23c4db)



🚀 Quick start:

Clone / download this repo and open DHT_Blynk.ino in the Arduino IDE.

Replace the placeholders with your own:
char ssid[] = "YOUR_WIFI_SSID";
char pass[] = "YOUR_WIFI_PASS";
#define BLYNK_AUTH_TOKEN "YOUR_BLYNK_TOKEN"

Select board & COM‑port
Tools ▸ Board ▸ NodeMCU 1.0 (ESP‑12E)
Tools ▸ Port ▸ COM…

Upload ➜ open Serial Monitor @ 9600 baud.

In the Blynk App or Web Dashboard, add two value widgets:
V0 → Temperature, V1 → Humidity.

📝 Serial output (example):
DHT Test Successful!
Blynk Connected Successfully
Humidity:  58.00%
Temperature: 25.20 °C

📁 File structure:
.
├── DHT_Blynk.ino     ← main sketch
└── README.md         ← this file

⚠️ Security notice
Your Wi‑Fi credentials and Blynk token are in plain text in the sketch.
Do not commit real secrets to a public repository—use environment variables or the Blynk “config template” feature for production.

📜 License
This project is released under the MIT License – see LICENSE for details.

Happy hacking! 🔥

