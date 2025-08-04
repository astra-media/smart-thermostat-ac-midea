# Smart Thermostat for Midea MAT12R1YWT Air Conditioner – IoT Project

## About this Project

This IoT project enables users to remotely control the temperature and power state of the **Midea MAT12R1YWT** air conditioner without modifying the A/C’s control unit—making it a non-invasive, safe, and energy-efficient solution.

Built on the **Arduino IoT Cloud** and powered by an **ESP32 development board**, the system is designed for both local and remote operation. The code includes **Alexa-compatible variables**, allowing control via **Amazon Alexa** voice commands.

Thanks to the ESP32’s **dual-core CPU**, the project can run two concurrent loops: one core handles cloud services and user input, while the other manages the A/C’s logic based on user-defined settings. This allows for smooth performance without interruptions.

Additional features include:

* **"Follow Me" mode** – sends the temperature detected by a **DHT11 sensor** to the A/C, emulating the original remote’s sensor feature.
* **"Away Mode"** – automatically turns the A/C on or off if the space becomes too hot, helping conserve energy.

> 🔧 Note: The code also includes variables for other devices not described in this section.

## Operation

The A/C is controlled via **infrared (IR) remote commands**, using the `IRremoteESP8266` library and its high-level `IRMideaAC` class. This allows for **stateful control** (like an actual remote) rather than sending raw hexadecimal codes.

The ESP32 uses:

* An **IR LED** to transmit commands,
* A **DHT11 sensor** to monitor room temperature, and
* An **LCD** to display system status.

**Push-buttons** are also included for manual, local control of the A/C unit.

## Components Used

Below is a list of the hardware components used in this project. For wiring diagrams and specifications, please refer to each component’s official datasheet.

* ESP32 Development Board
* DHT11 Temperature and Humidity Sensor
* Liquid Crystal Display (LCD)
* IR LED
* Push-buttons
* PCB Prototype Board