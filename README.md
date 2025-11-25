# Automatic Railway Gate (IoT)

**Cost-effective IoT-based automatic railway gate system** that detects approaching trains and performs safe, automatic gate closure with visual & audible alerts. Built with NodeMCU (ESP8266), IR sensors, servo motors, and IoT monitoring via the Blynk platform.  

> Demonstrates real-time detection, fast actuation (<5s), remote monitoring and a low-cost alternative to manual gate operation. :contentReference[oaicite:2]{index=2}

---

## Demo / Slides
The project presentation (architecture, workflow, test results) is available here:  
**`Automatic Railway Gate.pptx`** — `./Automatic Railway Gate.pptx`. :contentReference[oaicite:3]{index=3}

---

## Project Overview
Manual gate operation at unmanned railway crossings causes delays and accidents. This project automates gate control using sensor detection and microcontroller actuation to:

- Detect approaching trains using IR sensors.  
- Trigger servo motors to close/open the gate within ~5 seconds of detection.  
- Provide LED and buzzer alerts for pedestrians/vehicles.  
- Stream gate status and alerts to a mobile dashboard via Blynk (IoT).  
- Achieve a low-cost, low-maintenance solution suitable for rural and semi-urban crossings. :contentReference[oaicite:4]{index=4}

---

## Tech Stack
- **Microcontroller:** NodeMCU (ESP8266)  
- **Sensors:** IR sensors (HC-SR501 or equivalent)  
- **Actuators:** Servo Motor (SG90 / compatible)  
- **IoT Platform:** Blynk App (Wi-Fi status & remote monitoring)  
- **Support Hardware:** LEDs, Buzzers, Breadboard, Jumper wires  
- **Tools:** Tinkercad (simulation), VS Code (code editing) :contentReference[oaicite:5]{index=5}

---

## Key Features
- **Real-time train detection** using IR sensors with high lab accuracy (~98%). :contentReference[oaicite:6]{index=6}  
- **Fast response time** (gate close within 5 seconds of detection). :contentReference[oaicite:7]{index=7}  
- **Audible and visual alerts** (buzzers + LEDs) to warn pedestrians.  
- **IoT monitoring** through Blynk for remote status updates.  
- **Low cost** — hardware choices and design reduce cost ~76% vs typical manual/complex systems (lab analysis). :contentReference[oaicite:8]{index=8}

---

## System Architecture (High Level)
1. **Sensing Layer** — IR sensors detect incoming train signatures.  
2. **Processing Layer** — NodeMCU reads sensor input, debounces signal, and decides action.  
3. **Actuation Layer** — Servo motor executes gate close/open; LEDs and buzzer alert people.  
4. **IoT Layer** — NodeMCU posts status updates to Blynk (mobile UI). :contentReference[oaicite:9]{index=9}

---

## Implementation Notes
- **Sensor logic:** use simple threshold/distance logic with debounce to avoid false triggers.  
- **Servo control:** calibrate servo travel for full gate closure (0–180° depends on linkage).  
- **Alerts:** buzzer + LED activate before closing to allow safe stopping.  
- **IoT integration:** publish `gate_status`, `last_event_timestamp`, and `sensor_reading` to Blynk.  
- **Power:** choose stable 5V supply for NodeMCU + servo (use separate supply for servo if needed). :contentReference[oaicite:10]{index=10}

---

## Performance / Results
- **Response Time:** Gates close within ~5 seconds of detection (lab). :contentReference[oaicite:11]{index=11}  
- **Accuracy:** ~98% success rate in controlled testing. :contentReference[oaicite:12]{index=12}  
- **Cost Reduction:** Prototype design reduces estimated system cost compared to manual/complex alternatives (lab estimate). :contentReference[oaicite:13]{index=13}

---

## Files in This Repository
- `Automatic Railway Gate.pptx` — Project slides (architecture, implementation, test results). :contentReference[oaicite:14]{index=14}  
- `README.md` — This document.  
- `code/` — (Optional) Arduino/NodeMCU sketch files and configuration (create & add).  
- `schematics/` — (Optional) Wiring diagrams and block diagrams (create & add).  
- `data/` — (Optional) Test logs and performance data (create & add).

---

## How to Run (Prototype)
1. Upload the NodeMCU sketch to your ESP8266 (use Arduino IDE or PlatformIO).  
2. Connect IR sensor Vcc/GND/Signal to NodeMCU GPIO pin.  
3. Connect servo to PWM pin (and separate 5V power if necessary).  
4. Configure Blynk credentials and server token in the sketch.  
5. Place IR sensors at the recommended detection ranges and test with sample triggers.  
6. Calibrate servo angles and alert timers as required. :contentReference[oaicite:15]{index=15}

---

## Future Improvements
- Replace IR with more robust sensors (radar / LIDAR / ultrasonic hybrid) for weather tolerance.  
- Add solar power support for remote installations.  
- Add predictive analytics (ML) to estimate train speed & safety margins.  
- Add secure telemetry & remote administration features.

---

## Credits & Acknowledgements
- Project contributors and students (see slides for full team). :contentReference[oaicite:16]{index=16}  
- Academic guidance and department resources used during implementation. :contentReference[oaicite:17]{index=17}

---

## Contact
For questions, code requests, or collaboration:  
**Email:** narasimhavamsibhupathi@gmail.com 
(See project resume for additional contact & internship details). :contentReference[oaicite:18]{index=18}

---
