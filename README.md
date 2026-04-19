##  Overview

A **Buck Converter** is a high-efficiency DC-DC power converter used to step down voltage using high-frequency switching elements.

It is widely used in:

* Power supplies
* Embedded systems
* Battery-operated devices
* Voltage regulation modules (VRMs)

---

##  Operating Principle

The converter operates in two switching states:

**1. Switch ON (MOSFET Conducting):**

* Inductor stores energy
* Inductor current increases linearly
* Load is powered by source + inductor

**2. Switch OFF (MOSFET OFF, Diode Conducting):**

* Inductor releases stored energy
* Current continues through diode
* Output is maintained

---

##  Fundamental Relationship

[
V_{out} = D \cdot V_{in}
]

Where:

* (D) = Duty Cycle
* (V_{in}) = Input Voltage
* (V_{out}) = Output Voltage

---

##  Project 01 — Open Loop Buck Converter (12V → 5V)

###  Design Specifications

| Parameter           | Value  |
| ------------------- | ------ |
| Input Voltage       | 12V    |
| Output Voltage      | ~5V    |
| Load Resistance     | 2.5Ω   |
| Output Current      | 2A     |
| Switching Frequency | 50 kHz |
| Duty Cycle          | ~0.45  |

---

### ⚙️ Component Selection

| Component | Value     | Purpose                            |
| --------- | --------- | ---------------------------------- |
| Inductor  | 300 µH    | Energy storage & current smoothing |
| Capacitor | 22 µF     | Output voltage filtering           |
| MOSFET    | Switch    | High-speed switching element       |
| Diode     | Freewheel | Current path during OFF state      |

---

### Simulation Results

* Output voltage stabilizes at approximately **5V**
* Low output ripple observed
* Startup transient includes minor overshoot
* System achieves steady-state quickly

---

##  Key Learnings

* Output voltage is directly controlled by duty cycle
* Inductor dynamics govern current ripple behavior
* Output capacitor determines voltage ripple
* Switching frequency impacts efficiency and ripple
* Open-loop systems lack regulation under varying load conditions

---

##  Design Limitations

* No feedback mechanism (open-loop operation)
* Ideal components used in simulation (no losses modeled)
* Not directly suitable for real-world deployment without control system

---

##  Future Work

* Closed-loop control using feedback (PID / PWM controller)
* Efficiency and loss analysis
* Synchronous rectification implementation
* Thermal and power optimization
* Hardware prototyping and validation

---

##  Tools & Environment

* **LTspice** – Circuit simulation
* **GitHub** – Documentation and version control

---

##  Author

**Pruthvik S**
Power Electronics Learner | Embedded Systems Enthusiast

---
