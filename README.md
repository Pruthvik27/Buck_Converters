## 🚀 Project Roadmap

* [x] Open Loop Buck Converter (12V → 5V)
* [ ] Closed Loop Buck Converter (Feedback Control)
* [ ] Synchronous Buck Converter
* [ ] High Power Buck Converter
* [ ] Hardware Implementation

---

## 📂 Folder Structure

```
Buck_Converters/
│
├── 01_Open_Loop_12V_to_5V/
├── 02_Closed_Loop/
├── 03_Synchronous_Buck/
├── 04_High_Power/
```

---

##  What is a Buck Converter?

A **Buck Converter** is a DC-DC converter used to step down voltage efficiently using switching components like a MOSFET, diode, inductor, and capacitor.

---

## Working Principle

A buck converter operates in two states:

* **ON State (Switch ON):**

  * Inductor stores energy
  * Current increases

* **OFF State (Switch OFF):**

  * Diode conducts
  * Inductor releases energy to the load

---

##  Key Formula

[
V_{out} = D \cdot V_{in}
]

Where:

* (D) = Duty Cycle
* (V_{in}) = Input Voltage
* (V_{out}) = Output Voltage

---

##  Project 1: Open Loop Buck Converter (12V → 5V)

###  Specifications

* Input Voltage: 12V
* Output Voltage: ~5V
* Load Resistance: 2.5Ω
* Switching Frequency: 50kHz
* Duty Cycle: ~0.45

---

### Components Used

* MOSFET (Switch)
* Diode (Freewheeling)
* Inductor: 300µH
* Capacitor: 22µF

---

###  Observations

* Output voltage stabilizes around **5V**
* Small ripple present (expected)
* Initial overshoot during startup
* System reaches steady state quickly

---

##  What I Learned

* Duty cycle controls output voltage
* Inductor stores and releases energy
* Capacitor smooths output voltage
* Switching frequency affects ripple
* Open loop systems are not stable for real-world use

---

##  Limitations

* No feedback control (open loop)
* Ideal components used (no real losses)
* Not suitable for real hardware directly

---

##  Next Steps

* Implement closed-loop control
* Add PWM controller (Arduino / IC)
* Analyze efficiency
* Build real hardware prototype

---

##  Tools Used

* LTspice (Simulation)
* GitHub (Documentation)

---

##  Author

**Pruthvik S**
Learning Power Electronics 

---
