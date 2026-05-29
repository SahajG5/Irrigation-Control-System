# Irrigation Control System

> An Arduino-based smart irrigation controller that reads real-time environmental data and automatically regulates motor pump operation — deployed and tested on working farmland.

---

## Overview

India's agriculture sector is heavily dependent on rainfall, which has become increasingly irregular. This project addresses that challenge by implementing a sensor-driven irrigation controller that removes the need for constant manual supervision — allowing farmers to automate water delivery based on actual soil and environmental conditions.

The system was designed, built, and tested on real farmland, implementing both **Open Loop** and **Closed Loop** control strategies.

---

## Control System Design

### Open Loop Control
The farmer presets three parameters — amount of water, time of delivery, and frequency per day. The system then executes the irrigation schedule automatically without any real-time adjustments. Ideal for smaller, consistent farmlands where conditions don't change drastically.

**Advantages:** Low cost, simple to operate, no sensors required, runs unattended.  
**Limitation:** Does not adapt to changing environmental conditions like unexpected rain or soil saturation.

### Closed Loop Control
Sensors continuously measure soil moisture and environmental parameters. The controller reads this data in real time and makes irrigation decisions automatically — applying water only when and where needed.

**Advantage over open loop:** Self-correcting. The system responds to actual field conditions, preventing over- or under-watering and significantly optimizing water usage.

---

## How It Works

1. Sensors measure soil moisture, temperature, and humidity continuously.
2. The Arduino microcontroller reads and evaluates sensor data against preset thresholds.
3. If conditions require irrigation, the controller activates the motor pump.
4. Once the required moisture level is achieved, the pump is deactivated automatically.
5. The cycle repeats — with no manual intervention needed.

---

## Hardware

- Arduino Microcontroller Board
- Soil Moisture Sensor
- Temperature & Humidity Sensor
- Motor Pump + Relay Module
- Power Supply Unit
- Breadboard & connecting wires

---

## Project Structure

```
irrigation-control/
├── README.md
├── main.ino                  # Main Arduino sketch — control loop logic
├── sensors/
│   └── sensor_reader.ino     # Reads and processes sensor inputs
└── docs/
    └── circuit_diagram.png   # Hardware wiring reference
```

---

## Tech Stack

- **Platform:** Arduino
- **Language:** C++ (Arduino)
- **Components:** Microcontroller, soil moisture sensor, temperature sensor, relay, motor pump
- **Control Logic:** Open Loop + Closed Loop (sensor-feedback driven)

---

## Real-World Deployment

This system was not just a prototype — it was deployed and tested on actual farmland. The closed loop implementation demonstrated a measurable reduction in manual irrigation effort, with the motor pump responding autonomously to live soil moisture readings across varying weather conditions.

---

## Key Takeaway

By combining open loop scheduling with closed loop sensor feedback, this system provides a flexible, low-cost solution that adapts to real agricultural needs — making it practical even for farmers with limited technical backgrounds.
