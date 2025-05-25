
# 🕒 Bare-Metal I2C RTC Driver (Single File Implementation)

## 🎯 Objective
To implement a complete I2C driver from scratch without using any libraries and use it to interface with a DS1307 RTC module. All code is contained in a single C file and debugged using a logic analyzer.

## 🔧 Environment
- **MCU**: ATmega2560 (Arduino Mega)
- **Language**: Embedded C (no library used)
- **Debugger**: Logic Analyzer (e.g., Saleae)
- **Tool**: Arduino IDE / VS Code
- **Simulation**: Wokwi / Proteus

## ✅ Features
- Manual bit-banged I2C communication
- Start, Stop, Write, Read with ACK/NACK
- RTC time set and fetch functions
- Verified via logic analyzer (SCL/SDA signals)

## 📁 Project Structure
```
RTC_I2C_SingleFile/
├── main.c
├── README.md
├── logic_analyzer/
│   └── i2c_rtc_capture.sal
└── images/
    └── waveforms.png
```

## 🧠 Function Overview

### I2C Driver
```c
void i2c_start();
void i2c_stop();
void i2c_write(uint8_t data);
uint8_t i2c_read(uint8_t ack);
```

### RTC Functions
```c
void rtc_write(uint8_t reg, uint8_t data);
uint8_t rtc_read(uint8_t reg);
void rtc_set_time(...);
void rtc_get_time(...);
```

## 🔬 Debugging
- Verified with logic analyzer (SCL/SDA patterns)
- Ensured correct ACK from DS1307
- Matched waveform timing with datasheet specs

## 💻 Example Output (UART)
```
Time: 10:15:30 Date: 25/05/2024
```

## 📸 Sample Logic Analyzer Capture
![Waveform](images/waveforms.png)

## 🧑‍💻 Author
Your Name  
your.email@example.com | [GitHub](https://github.com/yourusername)
