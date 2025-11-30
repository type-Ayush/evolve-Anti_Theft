# 🔌 Circuit Wiring and Pinout: AI Anti-Theft Device

This document details the physical wiring connections of the AI Anti-Theft Device prototype.




---

## 1. Circuit Schematic 

For a clear visual guide to the placement and wiring of all components, refer to the following diagram:

![Detailed Wiring Schematic](assests\gallery\evolve-Anti_Theft_CIRCUIT.webp)

---

## 2. Pinout Table

The table below lists the required connections between the peripherals and the digital (D) or analog (A) pins of the Arduino Uno R3, based on the `firmware/AI_AntiTheft_Code.ino` file.

> **NOTE:** Please ensure your physical wiring matches these pin assignments for the code to function correctly.

| Component | Pin Function | Component Pin | Arduino Pin | Notes |
| :--- | :--- | :--- | :--- | :--- |
| **Power/Ground** | Power (VCC) | VCC | 5V | Common power connection. |
| | Ground (GND) | GND | GND | Common ground connection. |
| **OLED Display** | Data (SDA) | SDA | A4 | I<sup>2</sup>C Serial Data. |
| | Clock (SCL) | SCL | A5 | I<sup>2</sup>C Serial Clock. |
| **RTC Module** | Data (SDA) | SDA | A4 | I<sup>2</sup>C Serial Data (shared with OLED). |
| | Clock (SCL) | SCL | A5 | I<sup>2</sup>C Serial Clock (shared with OLED). |
| **Vibration Sensor** | Signal Out | D0 | D3 | Digital input for movement detection. |
| **Touch Sensor** | Signal Out | SIG | D4 | Digital input for contact detection (Uses internal pull-up). |
| **Ultrasonic Sensor**| Trigger Pin | Trig | D11 | Digital output to send ultrasonic pulse. |
| | Echo Pin | Echo | D10 | Digital input to receive echo pulse. |
| **Buzzer** | Signal Pin | B | D12 | Digital output for the audible alarm. |
| **Green LED** | Anode (+) | + | D13 | Indicates System is Armed and Safe. |
| **Orange LED** | Anode (+) | + | D6 | Indicates Suspicion (Casual Mode Alert). |
| **Red LED** | Anode (+) | + | D9 | Indicates Critical Alert (Sensitive Mode Alarm). |
| **Tactile Button** | Signal Pin | OUT | D8 | Used for the Action Menu and toggling modes (Uses internal pull-up). |
| **Mode Pin** |Mode Change|GND|D7|Plug pin to toggle mode|
| **Potentiometer** | Power  | Power | VCC | To Power the potentiometer|
| **Potentiometer** |Signal|Signal |`Buzzer (+)`| To control volume of the buzzer|


> **Note:** Please confirm the potentiometer Signal is connected to Buzzer (+)
<br><br>
> **Note:** Use Breadboard to make circuit, the above given is a schematic diagram is for to understand.Also use the resistor as instructed.



---

## 3. Component Details

* **OLED/RTC:** Both use the **I<sup>2</sup>C** bus, sharing pins A4 (SDA) and A5 (SCL).
* **Ultrasonic:** This sensor requires dedicated pins for the Trig (output) and Echo (input) functions.
