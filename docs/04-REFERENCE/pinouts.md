# Common Pinouts

Quick reference for common connectors and chips.

---

## Raspberry Pi GPIO

(image: raspberry-pi-gpio.jpg - GPIO pinout diagram)

Key pins:
- 3.3V power: Pins 1, 17
- 5V power: Pins 2, 4
- Ground: Pins 6, 9, 14, 20, 25, 30, 34, 39
- I2C: GPIO2 (SDA), GPIO3 (SCL)
- SPI: GPIO10 (MOSI), GPIO9 (MISO), GPIO11 (CLK)
- UART: GPIO14 (TX), GPIO15 (RX)

---

## Arduino Nano

(image: arduino-nano-pinout.jpg - Nano pinout diagram)

Key pins:
- 5V and 3.3V power outputs
- VIN: Input voltage (7-12V)
- A0-A7: Analog inputs
- D0-D13: Digital I/O
- D3, D5, D6, D9, D10, D11: PWM capable
- A4 (SDA), A5 (SCL): I2C
- D10-D13: SPI

---

## USB-A Connector

(image: usb-a-pinout.jpg - USB-A pinout)

| Pin | Function | Color (typical) |
|-----|----------|----------------|
| 1 | +5V (VBUS) | Red |
| 2 | Data - | White |
| 3 | Data + | Green |
| 4 | Ground | Black |

---

## Common Voltage Regulators

### 7805 (TO-220 Package)

(image: 7805-pinout.jpg - 7805 pinout)

Left to right (front facing):
1. Input
2. Ground
3. Output (5V)

### AMS1117/LM1117 (SOT-223)

Left to right:
1. Ground / Adjust
2. Output
3. Input
Tab: Output

---

## 555 Timer

(image: 555-pinout.jpg - 555 timer pinout)

| Pin | Function |
|-----|----------|
| 1 | Ground |
| 2 | Trigger |
| 3 | Output |
| 4 | Reset |
| 5 | Control Voltage |
| 6 | Threshold |
| 7 | Discharge |
| 8 | VCC (Power) |

---

## Common I2C Addresses

| Device | Address |
|--------|--------|
| OLED displays (SSD1306) | 0x3C or 0x3D |
| Temperature sensors (BMP280) | 0x76 or 0x77 |
| Real-time clock (DS3231) | 0x68 |
| EEPROM (AT24C32) | 0x50-0x57 |
| Accelerometer (MPU6050) | 0x68 or 0x69 |

---

## Communication Protocols Quick Reference

### I2C

- Two wires: SDA (data), SCL (clock)
- Needs pull-up resistors (usually 4.7k)
- Multiple devices on same bus

### SPI

- Four wires: MOSI, MISO, CLK, CS
- Faster than I2C
- Separate CS line for each device

### UART

- Two wires: TX, RX
- Cross-connect: TX to RX, RX to TX
- Common baud rates: 9600, 115200

---

[Back to Component Codes](component-codes.md) | [Troubleshooting](troubleshooting.md)
