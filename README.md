## smart_irrigation_system
A smart irrigation simulation using Cisco Packet Tracer

# Smart Irrigation System – Cisco Packet Tracer Simulation

## 🔍 Aim
To design a smart irrigation system using IoT devices in Cisco Packet Tracer that automatically manages a lawn sprinkler, humidifier, and water drain based on sensor data.

## ❓ Problem Statement
Traditional irrigation systems waste water by running at fixed times. This project creates an automated solution that reacts dynamically to environmental conditions, optimizing water use and improving efficiency.

## 🎯 Scope of the Solution
- Automate irrigation based on **humidity** and **water level**
- Trigger sprinkler, drain, and humidifier without manual intervention
- Visual and interactive simulation using Cisco Packet Tracer
- Scalable logic through Home Gateway and IoT Monitor interface

## 🏗️ Overview of the Architecture
The system is built using Cisco Packet Tracer’s IoT capabilities. All sensor and actuator devices are connected wirelessly to a **DLC100 Home Gateway** using WPA2-PSK encryption for secure communication. The gateway links to a **smartphone** that runs the **IoT Monitor App**, where logical conditions are defined.  
The simulation includes:
- A **Humidity Monitor** and **Water Level Monitor** to sense environmental changes
- A **Sprinkler**, **Humidifier**, and **Drain** as actuators
- All logic is processed via the gateway and executed based on real-time sensor data

## 🧠 Logical Conditions Implemented

| Condition Name   | Condition Description                                      | Action Performed            |
|------------------|------------------------------------------------------------|-----------------------------|
| `Hum_on`         | Hum_mon Humidity > 45%                                     | Turn ON Humidifier (Hum_1) |
| `Hum_off`        | Hum_mon Humidity between 30% and 40%                       | Turn OFF Humidifier (Hum_1)|
| `Sprink_on`      | Wat_mon Water Level < 3.0 cm                               | Turn ON Sprinkler (Sprink_1) & Turn OFF Drain_1 |
| `Sprink_off`     | Wat_mon Water Level >= 15.0 cm                             | Turn OFF Sprinkler (Sprink_1) |
| `Drain_off`      | Wat_mon Water Level is between 3.0 cm and 15.0 cm          | Turn OFF Drain_1            |
| `Drain_on`       | Wat_mon Water Level >= 20.0 cm                             | Turn ON Drain_1             |

## 🧱 Components Used

- **Water Level Monitor** – `Wat_mon`
- **Humidity Monitor** – `Hum_mon`
- **Lawn Sprinkler** – `Sprink_1`
- **Humidifier** – `Hum_1`
- **Water Drain** – `Drain_1`
- **DLC100 Home Gateway**
- **Smartphone** – For IoT Monitoring & Logic Configuration
