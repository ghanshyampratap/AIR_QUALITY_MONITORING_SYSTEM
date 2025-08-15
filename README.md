# 🌍 Air Quality Monitoring System

## 📖 Overview
The **Air Quality Monitoring System** is a low-cost, portable device designed to measure and display key environmental parameters in real-time.  
It uses **DHT11** for temperature & humidity, **MQ135** for harmful gases, and **GP2Y1010AU0F** for particulate matter (dust) detection, all controlled by an **Arduino Nano** with data displayed on a **0.96" OLED**.


## ✨ Features
- 📡 **Real-time monitoring** of:
  - Temperature (°C)
  - Humidity (%)
  - Gas concentration (general air pollutants)
  - Dust density (µg/m³)
- 💰 Low-cost & easy to assemble
- 🔌 Compact & portable design
- 📟 Live OLED display output
- 🔄 Modular design for easy upgrades (Wi-Fi, SD card logging, cloud integration)


## 🛠 Components Used
| Component | Purpose |
|-----------|---------|
| **Arduino Nano** | Central microcontroller |
| **DHT11** | Temperature & humidity sensor |
| **MQ135** | Multi-gas sensor (CO₂, NH₃, NOx, smoke, alcohol) |
| **GP2Y1010AU0F** | Optical dust sensor for PM detection |
| **SSD1306 OLED (0.96")** | Real-time display |
| **Breadboard & jumper wires** | Prototyping |
| **Power supply** | USB or 9V adapter |


## 🔌 Circuit Connections
| Sensor | Pin |
|--------|-----|
| **DHT11** | Data → D4 (10kΩ pull-up to 5V) |
| **MQ135** | AO → A1 |
| **GP2Y1010AU0F** | Vo → A0, LED control → D3 (150Ω resistor) |
| **OLED** | SDA → A4, SCL → A5 |

## 📦 Block Diagram
![Block Diagram](<img width="621" height="306" alt="image" src="https://github.com/user-attachments/assets/c8852ff4-3f03-4a95-819b-5a406f0efccd" />
)

## 📜 How It Works
1. Sensors collect environmental data.
2. Arduino Nano processes readings.
3. Dust sensor uses **timed LED pulses** for accurate particulate readings.
4. Gas sensor outputs voltage proportional to pollutant concentration.
5. Temperature & humidity are read digitally from DHT11.
6. Results are displayed on OLED in real-time and can be viewed via Serial Monitor.

## 🚀 Setup & Upload
1. Install the **Arduino IDE**.
2. Install required libraries:
   - `Adafruit_GFX`
   - `Adafruit_SSD1306`
   - `DHT sensor library`
3. Select **Arduino Nano** board in Tools → Board.
4. If using a clone Nano, set **Processor → ATmega328P (Old Bootloader)**.
5. Select correct **COM Port**.
6. Upload the provided `.ino` file.

## 📈 Results
- **Quick response** to smoke/dust introduction.
- **Stable baseline** in clean air.
- Detected **temperature & humidity** changes in real time.
- Works well for **indoor monitoring** and educational purposes.
  
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1cf8eef0-4a87-4939-9175-50210219eb66" />

![WhatsApp Image 2025-08-16 at 01 05 36_a429da44](https://github.com/user-attachments/assets/8bd906b5-dbfa-4ac9-9a85-f8a9915f8846)

![WhatsApp Image 2025-08-16 at 01 09 16_66223710](https://github.com/user-attachments/assets/eb6c42f2-c98e-446d-9792-5f24cc067813)

![WhatsApp Image 2025-08-16 at 01 09 16_a8c920a6](https://github.com/user-attachments/assets/43ebf47e-ae2f-4a7f-87bd-4411aee32e3f)


## 📈 Results
- **Quick response** to smoke/dust introduction.
- **Stable baseline** in clean air.
- Detected **temperature & humidity** changes in real time.
- Works well for **indoor monitoring** and educational purposes.

## 🔮 Future Improvements
- Wi-Fi / Bluetooth data transmission
- SD card data logging
- Mobile app & cloud dashboard
- More accurate laser dust sensor
- Dedicated sensors for specific gases



