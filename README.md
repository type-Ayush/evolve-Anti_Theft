# 🛡️ AI BASED IMMOBILE ANTI-THEFT TRACKING DEVICE

## 📝 1. Overview and Description

An **AI‑based immobile anti‑theft device** that monitors and tracks stationary assets, detects unauthorized movement, and provides real‑time alerts data to prevent theft and aid recovery. This device is designed for assets where any unauthorized movement, vibration, or tampering must be immediately flagged.

---

## ✨ 2. Features

* **Movement Detection:** Continuously monitors for **motion, vibration, and touch data** using multiple sensors to detect unauthorized movement or tampering.
* **Dual Monitoring Stages:** Operates in two customizable modes: **Casual** (Suspicion Alert) and **Sensitive** (Critical Alarm).
* **Local Alert System:** Provides immediate, local alerts to security personnel via an audible **Buzzer** and visual **LED indicator** (Red, Green, Orange).
* **Status Display:** Shows real-time device status, monitoring mode, and alert information on an **OLED Screen**.
* **Time-Stamped Data:** Utilizes an **RTC Module** for accurate time-stamping of all events and alerts.
* **Data Reporting:** Sends detection data and real-time alerts to a central control system (as detailed in the firmware).

---

## 📋 3. Components Required (Bill of Materials - BOM)


## 🔌 4. Wiring and Schematic



## ⚙️ 5. Installation and Setup

### Prerequisites (Libraries)
To compile the code, you must install the following libraries via the Arduino IDE's Library Manager:

* **`Adafruit GFX Library`** (By Adafruit)
* **`Adafruit SSD1306`** (By Adafruit, for the OLED display)
* **`RTClib`** (By Adafruit, for the Real-Time Clock module)
> **Note:** Libraries such as `Wire.h` (for I<sup>2</sup>C communication) and `EEPROM.h` (for permanent data storage) are standard libraries bundled with the Arduino IDE and do not require separate installation.

### Firmware Upload Instructions

1.  **Install the Arduino IDE:** Ensure you have the latest version installed on your computer.
2.  **Install Libraries:** Install all the required libraries listed above using the Arduino Library Manager.
3.  **Download the Sketch:** Download the main project sketch file, which you can find here: <!--link of arduino final file-->
4.  **Configure Board:** In the Arduino IDE, select **Tools > Board > Arduino Uno**.
5.  **Upload:** Connect your wired Arduino Uno R3 

<!--[Image of Arduino Uno R3]-->
 to your computer and click the **Upload** button.

---

## 💡 6. Usage

The device is designed for rapid deployment and features two operational modes to handle different risk environments.<br><br>
Please Refer: <!--Explaination.md link--> for more Information.
### Operational Workflow

1.  **Arming:** The system automatically gets **Armed** upon powering the device.
2.  **Safe State:** When armed and no threat is detected, the **Green LED** lights up, and the **OLED screen** displays:
    ```
    SYSTEM ARMED
    SAFE - Monitoring
    [Current Time & Date]
    ```

### Monitoring Modes

The system operates in two modes—**Casual** and **Sensitive**—which can be toggled using the **Tactile Push Button** to access an on-screen Action Menu.

| Mode | Trigger Response | Visual & Audible Alert |
| :--- | :--- | :--- |
| **Casual Mode** | Raises **Suspicion** (Low Risk) | **Orange LED** lights up. OLED displays `SUSPICION DETECTED`. No buzzer sound. |
| **Sensitive Mode** | Triggers **Critical Alert** (High Risk) | **Red LED** lights up. **Buzzer** sounds repeatedly. OLED displays `🚨 CRITICAL ALERT! MOTION DETECTED`. |

---

## 🧠 7. Code Logic and AI Implementation

The core state machine, sensor data processing, and the details of the AI-based theft prediction logic are documented separately to ensure clarity and focus in this README.

> For a complete breakdown of the device's state machine, sensor data processing, and the specific algorithms/logic used for **AI-based theft prediction**, please see the **`explanation.md`** file in the repository root.
>
> **➡️ <!--[Link to `explanation.md` here]**-->

---

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
