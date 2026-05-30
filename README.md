<div align="center">

<br/>

```
 ██████╗ ██████╗ ██████╗ ██╗ █████╗ 
██╔═══██╗██╔══██╗██╔══██╗██║██╔══██╗
██║   ██║██████╔╝██████╔╝██║███████║
██║   ██║██╔══██╗██╔══██╗██║██╔══██║
╚██████╔╝██║  ██║██████╔╝██║██║  ██║
╚══════╝ ╚═╝  ╚═╝╚═════╝ ╚═╝╚═╝  ╚═╝
```

### Embedded systems with purpose. From edge to panel, in real time.

*A [RovaTech](https://github.com/rovatech) project*

[🇧🇷 Português](./README.pt-BR.md) | 🇺🇸 English

[![Status](https://img.shields.io/badge/status-in_development-orange?style=flat-square)]()
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)]()
[![ESP+Lua](https://img.shields.io/badge/ESP-Lua-darkgreen?style=flat-square)]()
[![Tasmota](https://img.shields.io/badge/Tasmota-firmware-red?style=flat-square)]()
[![TouchDesigner](https://img.shields.io/badge/TouchDesigner-visual_engine-purple?style=flat-square)]()

</div>

---

## What is Orbia

**Orbia** is a suite of modular embedded systems developed by RovaTech, focused on four social impact domains: **home, accessibility, industry and education**.

Each system combines ESP firmware with Lua, load control via Tasmota and real-time visualization in TouchDesigner — forming a low-cost, open source and replicable architecture for anyone or any organization.

---

## Stack

| Layer | Technology | Role |
|---|---|---|
| **Edge / Firmware** | ESP8266 / ESP32 + Lua | Local processing, embedded logic |
| **Load control** | Tasmota | Relays, switches, automation via MQTT |
| **Visualization** | TouchDesigner | Dashboards, visual interfaces and real-time audiovisual |
| **Communication** | MQTT, HTTP REST, WebSocket | Inter-layer integration |
| **Sensors** | DHT22, HC-SR04, MPU6050, PIR, MQ-series | Environmental and motion data collection |

---

## Modules

### 🏠 Home — Advanced Residential Automation

#### Environmental Adaptation System
Motion, temperature, humidity and light sensors distributed throughout the residence. The ESP with Lua processes data locally, Tasmota controls loads and TouchDesigner generates a visual panel that **learns the family's habits** and automatically adjusts lighting, ventilation and security.
- Suspicious motion detection with night alerts
- Automatic environment adjustment by time and usage profile
- Real-time visual monitoring interface

#### Elderly Care System
Combines motion sensor, fall sensor, door monitoring and a simple camera. Detects if an elderly person has been still for too long, has fallen or left a door open — **projects visual alerts on the living room TV** and sends a notification to the family member's phone.
- Prolonged inactivity and fall detection
- TV and mobile device integration
- Event history for follow-up

---

### ♿ Accessibility — Deeper Inclusion

#### Sound and Visual Map for the Visually Impaired
Multiple ultrasonic and motion sensors create a **real-time map of the environment**. TouchDesigner transforms the data into directional sound (volume proportional to obstacle proximity) and visual projection for companions and educators.
- Assisted navigation in indoor environments
- Support for teachers in school and therapeutic contexts
- Applicable at home, school and public transport

#### Motion Control for Partial Paralysis
System that interprets complex gestures using `MPU6050 + Lua` to **control lights, TV, fan and trigger emergency calls**. TouchDesigner serves as a large visual interface for family members to follow executed commands.
- Full environment control by gestures
- Integrated emergency trigger
- Clear interface for family members and caregivers

---

### 🔧 Technical / Professional

#### Predictive Monitoring for Small Industries
Vibration, temperature and motion sensors on machines. The ESP with Lua pre-processes data, Tasmota controls safety relays and TouchDesigner generates a panel with **real-time charts, imminent failure alerts and usage history**.
- Predictive maintenance accessible to small factories and workshops
- Reduction of corrective maintenance and unplanned downtime
- Exportable data for further analysis

#### Quality Control System for Laboratories
Motion sensor + temperature + door opening. Detects unauthorized access, out-of-range temperature and equipment left on too long — **logging everything visually in TouchDesigner**.
- Environment compliance for labs and technical rooms
- Automated event and violation logging
- Real-time alerts via MQTT

---

### 🔬 Scientific and Educational

#### Community Environmental Monitoring Station
Network of ESPs with air quality, animal motion, temperature, humidity and CO2 sensors. Data is processed in Lua and sent to a **TouchDesigner dashboard with scientific visualizations**. Designed for schools, universities and NGOs.
- Pollution and conservation monitoring in neighborhoods
- Open and exportable data for research
- Low-cost installation with accessible hardware

#### Interactive Physics and Biology Lab
Students use motion, force and distance sensors to run advanced experiments. TouchDesigner displays **charts, simulations and real-time analysis** — turning theoretical classes into hands-on experiences without expensive equipment.
- Replaces high-cost lab equipment
- Intuitive interface for teachers and students
- Expandable with new sensors and experiments

---

## Repository structure

```
orbia/
├── home/
│   ├── environmental-adaptation/
│   └── elderly-care/
├── accessibility/
│   ├── sound-visual-map/
│   └── motion-control/
├── technical/
│   ├── predictive-monitoring/
│   └── lab-quality-control/
├── educational/
│   ├── environmental-station/
│   └── interactive-lab/
└── shared/
    ├── firmware/           # Reusable ESP+Lua base
    ├── tasmota-configs/    # Tasmota configuration templates
    └── td-patches/         # Base TouchDesigner patches
```

---

## How to contribute

```bash
# Clone the repository
git clone https://github.com/rovatech/orbia.git

# Navigate to the desired module
cd orbia/<domain>/<project>
cat README.md
```

1. **Fork** the repository
2. Create a branch: `git checkout -b feat/feature-name`
3. Commit: `git commit -m 'feat: clear description'`
4. Push: `git push origin feat/feature-name`
5. Open a **Pull Request**

---

## Developed by

**[RovaTech](https://github.com/rovatech)** — [@pedro-juno](https://github.com/pedro-juno) · [@ana-mouca](https://github.com/ana-mouca)

---

<div align="center">

**Orbia · RovaTech** — *From edge to panel, in real time.*

</div>
