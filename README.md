# ESP32 Google Assistant + Alexa + Manual Home Automation (Sinric Pro)

This project demonstrates how to control home appliances (like lights, fans, etc.) using an **ESP32**, with support for **Google Assistant**, **Amazon Alexa**, and **manual switches** through the **Sinric Pro IoT platform**.

With this setup, you can:

* Control appliances via **voice commands** (Google Assistant/Alexa).
* Control appliances manually using **switches/push buttons**.
* Control appliances via the **Sinric Pro mobile app** over WiFi.

---

## 🚀 Features

* Voice control via **Google Assistant** and **Amazon Alexa**.
* Mobile control using the **Sinric Pro App**.
* Manual ON/OFF control using **physical switches or push buttons**.
* Real-time synchronization of device states (app <-> ESP32 <-> voice assistants).
* Works over **WiFi** (no extra hardware required other than ESP32).
* Easily expandable for multiple appliances.

---

## 🛠 Hardware Required

* ESP32 Development Board
* 1-3 Channel Relay Module
* Appliances (Bulb/Fan etc. up to relay rating)
* Switches / Push Buttons
* Breadboard & Jumper wires

⚠️ **Note:** Handle AC connections carefully! Always insulate exposed wires and ensure safety when working with 230V AC.

---

## 📲 Software Required

* [Arduino IDE](https://www.arduino.cc/en/software)
* ESP32 board support installed in Arduino IDE
* [Sinric Pro account](https://sinric.pro/) (free to start)
* [Sinric Pro App](https://play.google.com/store/apps/details?id=pro.sinric.app) (Android/iOS)
* Required Libraries:

  * [ArduinoJson](https://github.com/bblanchon/ArduinoJson)
  * [SinricPro](https://sinricpro.github.io/esp8266-esp32-sdk/)
  * [arduinoWebSockets](https://github.com/Links2004/arduinoWebSockets)

---

## ⚙️ Circuit Connection

| ESP32 Pin | Device              |
| --------- | ------------------- |
| GPIO 15   | Relay 1 (Appliance) |
| GPIO 23   | Switch 1            |
| GPIO 2    | WiFi Status LED     |

*(Add Relay 2, Relay 3, Switch 2, Switch 3 if expanding the project)*

Relay Output side (AC):

* **COM → AC Live input**
* **NO → Appliance Live wire**
* **Neutral directly → Appliance Neutral**

---

## 💻 Code Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/esp32-sinricpro-homeautomation.git
   cd esp32-sinricpro-homeautomation
   ```

2. Open the code in **Arduino IDE**.

3. Update the following credentials in the code:

   ```cpp
   #define WIFI_SSID     "Your_WiFi_Name"
   #define WIFI_PASS     "Your_WiFi_Password"
   #define APP_KEY       "Your_SinricPro_APP_KEY"
   #define APP_SECRET    "Your_SinricPro_APP_SECRET"
   #define device_ID_1   "Your_Device_ID"
   ```

4. Select **ESP32 Dev Module** in Arduino IDE → Tools → Board.

5. Upload the code to ESP32.

6. Open **Sinric Pro App**, add a Switch device, and link it with Google Assistant or Alexa.

---

## 📷 Demo

### Circuit Diagram

<img width="638" height="361" alt="image" src="https://github.com/user-attachments/assets/5ea0b621-e743-46f0-a60a-fa793bd30cef" />


### Video Demo




https://github.com/user-attachments/assets/4355dadd-af83-4a3e-af80-54cf6b4faa8a


---

## 📝 License

This project is licensed under the MIT License – feel free to use and modify it.

---

