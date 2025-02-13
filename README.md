# **Custom 4-Bit Adder Design**  

This repository contains the **design, simulation, and verification** of a **custom 4-bit adder**. The design is optimized for **power, delay, and area**, ensuring compliance with given design constraints.  

## 📌 **Table of Contents**  

- [Introduction](#introduction)  
- [Design Specifications](#design-specifications)  
- [Design Approach](#design-approach)  
- [Schematic and Transistor Sizing](#schematic-and-transistor-sizing)  
- [Simulation Results](#simulation-results)  
- [DRC and LVS Verification](#drc-and-lvs-verification)  
- [Final Score](#final-score)  
- [Conclusion](#conclusion)  
- [Future Improvements](#future-improvements)  

---

## 📝 **Introduction**  

The goal of this project was to design a **4-bit adder** with optimized **power consumption, delay, and layout area** using **32nm technology**. The design is validated through **schematic simulation, layout verification (DRC & LVS), and performance evaluation**.  

---

## ⚙ **Design Specifications**  

- **Technology:** 32nm CMOS  
- **VDD:** 1.05V  
- **Transition Time (Tr):** 30ps (10%-90% of VDD)  
- **Load:** 4 minimum-sized inverters per output  
- **Minimum NMOS Size:** WN = 300nm  
- **Performance Targets:**  
  - **Delay:** < 400ps  
  - **Area:** < 150µm²  
  - **Power:** < 100µW  

---

## 🏗 **Design Approach**  

- A **1-bit full adder** was designed and optimized at the **transistor level**.  
- A **4-bit adder** was constructed by cascading four **1-bit full adders**.  
- Logic gates were designed with **appropriate transistor sizing** to balance **power and delay**.  
- **No additional scaling** was required, as the design met the required delay constraints.  

---

## 🖥 **Schematic and Transistor Sizing**  

### **1️⃣ Full Adder Schematic**  
- The **1-bit adder schematic** includes XOR, AND, and inverter gates.  
- The **4-bit adder schematic** is implemented using a ripple-carry architecture.  

### **2️⃣ Transistor Sizing**  
- The width-to-length ratio (W/L) of all transistors was chosen to balance performance and power.  
- **Minimum NMOS size used**: **WN = 300nm**  
- **WP was adjusted** to match **LH and HL delays** across all logic gates.  

### **3️⃣ Layout Design**  
- **Single-bit adder layout** and **full 4-bit adder layout** were designed.  
- Layout verification was conducted using **DRC and LVS checks**.  

---

## 🔬 **Simulation Results**  

### ✅ **Worst-Case Delay**  
- Measured **worst-case delay** between **A0 and S3**: **52.3ps**  

### ⚡ **Power Consumption**  
- Average power consumption: **68.6 µW**  

---

## ✅ **DRC and LVS Verification**  

### 📏 **Layout & DRC Check**  
- **1-bit adder and 4-bit adder layouts** were designed.  
- **DRC (Design Rule Check) passed** for both layouts.  

### 🔍 **LVS Check**  
- **LVS (Layout vs. Schematic) passed**, confirming the correctness of the layout.  

---

## 📊 **Final Score**  

The **performance score** was computed using the formula:

```
Score = (400ps / Delay) + (100µW / Power) + (150µm² / Area)
```

```
Score = (400ps / 52.3ps) + (100µW / 68.6µW) + (150µm² / 43.8µm²)
```

```
Final Score = 12.5
```

---

## 🏁 **Conclusion**  

- The **4-bit adder was successfully designed and verified** while meeting all required constraints.  
- The design **passed all DRC and LVS checks**, making it fabrication-ready.  
- The measured performance suggests an **efficient and optimized implementation** in terms of **power, delay, and area**.  

---

## 🚀 **Future Improvements**  

- **Further power optimization** through alternative logic styles.  
- **Pipelining techniques** to enhance speed.  
- **Floorplanning adjustments** for reduced layout area.  
