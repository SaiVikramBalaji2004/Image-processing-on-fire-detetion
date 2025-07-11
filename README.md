# 📷 How to Program ESP32-CAM

**Published on:** January 31, 2025  
**Author:** Jonahan  

The **ESP32-CAM** is a low-cost, powerful microcontroller board with built-in camera support, making it perfect for IoT projects such as video streaming, surveillance, and facial recognition. However, it lacks a built-in USB port, which makes programming a bit tricky.

This guide covers **two methods** to program the ESP32-CAM:

- ✅ Using an **Arduino Uno** as a programmer  
- ✅ Using an **FTDI programmer** (USB-to-TTL converter)

---

## 🧰 What You'll Need

### Common Items (Both Methods)
- ESP32-CAM Module  
- Jumper Wires  
- Breadboard (optional)  
- Arduino IDE (installed)

### For Method 1 (Arduino Uno)
- Arduino Uno  
- USB Cable (for Uno)

### For Method 2 (FTDI Programmer)
- FTDI Programmer / USB-to-TTL Converter  
- Micro-USB Cable (for FTDI)

---

## 🔧 Method 1: Programming ESP32-CAM Using Arduino Uno

### Step 1: Install the ESP32 Board Package

1. Open **Arduino IDE**  
2. Go to **File > Preferences**  
3. In **"Additional Boards Manager URLs"**, add:https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
4. Click **OK**
5. Go to **Tools > Board > Boards Manager**
6. Search for `esp32` and install **ESP32 by Espressif Systems**

### Step 2: Wire Arduino Uno to ESP32-CAM

| Arduino Uno | ESP32-CAM |
|-------------|-----------|
| 5V          | 5V        |
| GND         | GND       |
| TX (Pin 1)  | U0R       |
| RX (Pin 0)  | U0T       |
| GPIO0       | GND (for flashing) |

- Disconnect GPIO0 after uploading to run the code normally.
- circuit diagram
  ![image alt](https://github.com/SaiVikramBalaji2004/Image-processing-on-fire-detetion/blob/b1e9149b1eee7b5795b7c34898d234945ee787ca/image.png)

### Step 3: Upload Sample Code

```cpp
void setup() {
Serial.begin(115200);
}
void loop() {
Serial.println("Hello, ESP32-CAM!");
}


---

Let me know if you'd like it turned into a GitHub repo template with sample `platformio.ini`, images, or wiring diagrams.

![image alt](https://github.com/SaiVikramBalaji2004/Image-processing-on-fire-detetion/blob/9e23f8b3fc52b95172fbbe8d7005ca0a9ca4c754/ESP32-CAM%20real.jpg)
```
![image alt](https://github.com/SaiVikramBalaji2004/Image-processing-on-fire-detetion/blob/9e23f8b3fc52b95172fbbe8d7005ca0a9ca4c754/ESP32-CAM%20real.jpg)

