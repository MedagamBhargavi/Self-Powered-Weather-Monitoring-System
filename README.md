# Self-Powered Weather Monitoring System 🌦️☀️

An **IoT-based self-powered weather monitoring system** designed to collect and monitor environmental parameters such as **temperature, humidity, atmospheric pressure, and rainfall** in real time.

The system uses an **ESP8266 NodeMCU** as the main microcontroller. Environmental data is collected using sensors and transmitted through Wi-Fi to the **ThingSpeak cloud platform** for remote monitoring and analysis. The system is powered using a **solar panel and rechargeable Li-ion battery**, making it suitable for remote and off-grid environments.

## 📌 Project Overview

Traditional weather monitoring systems may depend on conventional power sources and may not be suitable for remote locations. This project addresses this limitation by combining **IoT technology with renewable solar energy**.

The system continuously collects environmental data from sensors, processes the readings using the ESP8266, and uploads the data to ThingSpeak through Wi-Fi.

According to the project report, the system is intended for applications such as **agriculture, environmental monitoring, climate research, and weather observation**.

## ✨ Features

* 🌡️ Temperature monitoring
* 💧 Humidity monitoring
* 🌬️ Atmospheric pressure monitoring
* 🌧️ Rainfall detection
* ☀️ Solar-powered operation
* 🔋 Rechargeable Li-ion battery backup
* 📡 Wi-Fi-based data transmission
* ☁️ ThingSpeak cloud monitoring
* 📊 Real-time environmental data collection
* 🔌 Low-power operation
* 🌱 Renewable-energy-based system

## 🛠️ Hardware Components

| Component                     | Purpose                                       |
| ----------------------------- | --------------------------------------------- |
| **ESP8266 NodeMCU**           | Main microcontroller and Wi-Fi communication  |
| **DHT11 Sensor**              | Measures temperature and humidity             |
| **BMP280 Sensor**             | Measures atmospheric pressure and temperature |
| **Rain Sensor**               | Detects rainfall/moisture                     |
| **6V Solar Panel**            | Generates renewable electrical energy         |
| **3.7V 18650 Li-ion Battery** | Stores electrical energy                      |
| **TP4056 Charger Module**     | Charges the Li-ion battery                    |
| **DC-DC Step-Up Booster**     | Boosts the input voltage                      |
| **Jumper Wires**              | Connects the electronic components            |

The component list is based on the hardware specified in the project report.

## ⚙️ Working Principle

The system works through the following steps:

1. The **solar panel** generates electrical energy.
2. The generated energy is used to charge the **Li-ion battery** through the charging circuit.
3. The **ESP8266 NodeMCU** acts as the main controller.
4. The **DHT11** collects temperature and humidity data.
5. The **BMP280** collects atmospheric pressure and temperature data.
6. The **rain sensor** detects rainfall conditions.
7. The ESP8266 processes the sensor readings.
8. The ESP8266 connects to the Internet using Wi-Fi.
9. The collected data is uploaded to **ThingSpeak**.
10. The data can then be monitored and analyzed remotely.

The report describes the ESP8266 as the controller responsible for processing sensor data and transmitting it to ThingSpeak.

## 🔄 System Flow

```text
                 ☀️ Solar Panel
                       │
                       ▼
                🔋 Li-ion Battery
                       │
                 TP4056 Charger
                       │
                       ▼
              ⚡ Power Management
                       │
                       ▼
                ESP8266 NodeMCU
                 │      │      │
                 │      │      │
                 ▼      ▼      ▼
              DHT11  BMP280  Rain Sensor
                 │      │      │
                 └──────┼──────┘
                        ▼
                  Sensor Data
                        │
                        ▼
                    Wi-Fi
                        │
                        ▼
                  ThingSpeak
                        │
                        ▼
             📊 Remote Monitoring
```

## 💻 Software & Technologies

* **Arduino IDE**
* **Embedded C/C++**
* **ESP8266 NodeMCU**
* **ThingSpeak**
* **Wi-Fi**
* **IoT**
* **DHT11**
* **BMP280**

The project code uses libraries including `Adafruit_BMP280`, `DHT`, `ESP8266WiFi`, `Wire`, and `ThingSpeak`.

## 📂 Project Structure

```text
Self-Powered-Weather-Monitoring-System/
│
├── README.md
│
├── src/
│   └── weather_monitoring.ino
│
├── hardware/
│   └── circuit_diagram.png
│
├── images/
│   ├── project_setup.jpg
│   ├── esp8266.jpg
│   ├── dht11.jpg
│   ├── bmp280.jpg
│   └── rain_sensor.jpg
│
└── docs/
    └── Project_Report.pdf
```

## 📊 Data Monitoring

The ESP8266 sends sensor readings to different ThingSpeak fields:

```text
Field 1 → BMP280 Temperature
Field 2 → Atmospheric Pressure
Field 3 → DHT11 Humidity
Field 4 → DHT11 Temperature
Field 5 → Rain Sensor Value
```

These field assignments are specified in the project code included in the report.

## 🎯 Applications

This project can be useful for:

* 🌾 Smart agriculture
* 🌦️ Weather monitoring
* 🌱 Environmental monitoring
* 🚨 Weather-related safety monitoring
* 🏞️ Remote/off-grid locations
* 🔬 Climate research
* 📡 IoT-based monitoring systems

The report identifies agriculture, environmental monitoring, climate research, and emergency management among the potential application areas.

## 🚀 Future Enhancements

Possible future improvements include:

* Integration with **AI-based weather prediction**
* Adding more environmental sensors
* Improving solar power management
* Adding a mobile application
* Adding weather alerts and notifications
* Expanding the system to multiple monitoring nodes
* Improving remote monitoring capabilities
* Using advanced analytics for collected weather data

The project report also identifies integration with emerging technologies, scalability, and interdisciplinary applications as future directions.

## 📈 Project Outcome

The developed system demonstrates how **IoT, environmental sensors, wireless communication, cloud monitoring, and renewable energy** can be combined to create a self-powered weather monitoring solution.

The project provides real-time environmental data while reducing dependence on conventional power sources through solar energy.

## 👩‍💻 Team Member

* **M. Bhargavi**
  
Project completed as part of **Design Thinking and Innovation** at **Vasireddy Venkatadri Institute of Technology (VVIT)** under the guidance of **Dr. S. Krishna Prasad, Professor**.

## 📄 Project Report

The complete project report is available in the `docs` folder.

## ⚠️ Configuration

Example:

```cpp
const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";

unsigned long channelID = YOUR_CHANNEL_ID;
const char* writeAPIKey = "YOUR_THINGSPEAK_API_KEY";
```

## 📚 Reference

The project report references resources related to the NodeMCU/ESP8266 and ThingSpeak-based solar weather monitoring system.

---

⭐ **If you found this project useful, consider giving the repository a star!**
