
# 🕒 Bare-Metal I2C RTC Driver (Single File Implementation)

## 🎯 Objective
To implement a complete I2C driver from scratch without using any libraries and use it to interface with a DS1307 RTC module. All code is contained in a single C file and debugged using a logic analyzer. RTC is connected to portf 0(SDA) 1(SCL).
## 🔧 Environment
- **MCU**: ATmega2560 (Arduino Mega)
- **Language**: Embedded C (no library used)
- **Debugger**: Logic Analyzer 
- **Tool**: Arduino IDE 
- **Simulation**: Wokwi 

## ✅ Features
- Manual bit-banged I2C communication
- Start, Stop, Write, Read with ACK/NACK
- RTC time set and fetch functions
- Verified via logic analyzer (SCL/SDA signals)

## 🧠 Function Overview

### I2C Driver
```c
void I2C_start();
void I2C_write(char);
void I2C_delay();
void I2C_stop();
char I2C_read();
```

### RTC Functions
```c
void RTC_write(char,char);
char RTC_read(char);
```

## 🔬 Debugging
- Verified with logic analyzer (SCL/SDA patterns)
- Ensured correct ACK from DS1307
- Matched waveform timing with datasheet specs

## 💻 Example Output (UART)
```
Time :23/59/28
```



## 🧑‍💻 Author
Your Bhuvan Kumar R P 
your.kumarrpbhuvan@gmail.com | [GitHub](https://github.com/Bhuvan-Kumar-R-P)
