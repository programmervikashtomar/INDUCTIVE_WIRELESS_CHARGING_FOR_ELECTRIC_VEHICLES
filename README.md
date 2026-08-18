# INDUCTIVE_WIRELESS_CHARGING_FOR_ELECTRIC_VEHICLES — Inductive Power Transfer & Battery Charging Simulation

A MATLAB/Simulink model for studying **inductive power transfer, power-electronic conversion, and battery charging** using a three-phase AC source, switching converters, transformer, RLC components, measurement blocks, and a lithium-ion battery.

The model is developed for simulation and analysis of power-flow and charging behavior in an electrically controlled power-transfer system.

---

## 📌 Project Overview

`INDUCTIVE_WIRELESS_CHARGING_FOR_ELECTRIC_VEHICLES.slx` is a Simulink-based power-electronics model designed to simulate the complete energy path from an AC power source to a rechargeable battery.

The model combines power conversion, switching control, transformer coupling, RLC components, electrical measurements, and battery dynamics.

It can be used for studying **inductive charging systems, EV charging concepts, converter behavior, voltage/current characteristics, and battery charging performance**.

---

## ⚡ Main System

The model contains the following major stages

        THREE-PHASE AC SOURCE
                  │
                  ▼
       AC POWER / MEASUREMENT
                  │
                  ▼
          POWER CONVERTER
       (IGBT / Diode Bridge)
                  │
                  ▼
       RESONANT / RLC NETWORK
                  │
                  ▼
        LINEAR TRANSFORMER
                  │
                  ▼
        RECTIFICATION STAGE
                  │
                  ▼
          PWM DC-DC CONTROL
                  │
                  ▼
              BATTERY
          (Li-Ion Model)
```

---

## 🔧 Main Components

### 1. Three-Phase Source

The model uses a **Three-Phase Source** as the primary electrical supply. This provides the AC input required by the power-electronic conversion stage.

### 2. Power Electronic Switching

IGBT/Diode devices are used for controlled switching and power conversion. The switching stage allows the electrical power delivered to the downstream circuit to be controlled.

### 3. RLC / Resonant Network

Several **Series RLC Branch** elements are included in the model. These components are important for modeling resonant behavior and energy transfer in the power-transfer section.

### 4. Linear Transformer

A **Linear Transformer** provides electrical isolation and voltage transformation between sections of the system. It is also used to represent the coupling mechanism of the power-transfer stage.

### 5. PWM DC-DC Converter

A **PWM Generator (DC-DC)** provides the switching control required for DC-side power regulation. PWM control can be used to regulate the voltage/current supplied to the battery.

### 6. Lithium-Ion Battery

The model contains a **Lithium-Ion Battery** block representing the energy-storage system.

The configured battery model includes:

| Parameter        |    Value |
| ---------------- | -------: |
| Nominal Voltage  |    350 V |
| Nominal Capacity |   150 Ah |
| Initial SOC      |      99% |
| Minimum Voltage  |  262.5 V |
| Full Voltage     | ~407.4 V |

These parameters can be modified according to the battery and charging application being investigated.

---

## 📊 Measurement & Monitoring

The model includes several measurement and visualization blocks for monitoring system behavior.

### Measurements

* Current Measurement
* Voltage Measurement
* Three-Phase V-I Measurement
* Three-Phase Power Measurement
* Powergui
* Multiple Scopes
* Display blocks

These measurements can be used to observe:

* Input voltage
* Input current
* Output voltage
* Charging current
* Battery voltage
* Power flow
* Switching/converter behavior
* Charging characteristics

If you find this Simulink model useful for your research, project, or learning, consider giving the repository a ⭐ on GitHub.
