# STM32-ST7789-TFT-Hello-Display
A basic STM32 project demonstrating how to interface an ST7789 TFT display using SPI and DMA, and display text on the screen.
# STM32 ST7789 TFT Display (Hello World)

## About this project

This project demonstrates how to interface a **TFT display (ST7789)** with STM32 using SPI communication.

The goal was to understand how graphical displays work and how to send data efficiently using SPI and DMA.

In this project, I successfully displayed a simple **"Hello!"** message on the TFT screen.

---

## What it does

* Initializes ST7789 TFT display
* Uses SPI communication (high-speed)
* Uses DMA for efficient data transfer
* Clears screen and sets background color
* Displays text on screen

---

## How it works (simple)

1. STM32 initializes SPI and DMA
2. TFT display is initialized using driver
3. Screen is cleared (black background)
4. Text is sent to display using SPI
5. Display shows the message

So basically:

STM32 → SPI → TFT Display → Text Output

---

## Output

The TFT screen shows:

Hello!

Displayed at position (20, 50) with white text on black background.

---

## Hardware Used

* STM32F103C8T6 (Blue Pill)
* ST7789 TFT Display
* SPI Interface

---

## Pin Configuration (Typical)

| TFT Pin | STM32 Pin  |
| ------- | ---------- |
| SCL     | SPI Clock  |
| SDA     | SPI MOSI   |
| DC      | GPIO (PA1) |
| RST     | GPIO (PA0) |
| CS      | GPIO (PA2) |

(Note: Pins may vary based on your setup)

---

## Important Code

### Display Initialization

```c
ST7789_Init();
ST7789_Fill_Color(BLACK);
```

### Display Text

```c
ST7789_WriteString(20,50,"Hello!",Font_11x18,WHITE,BLACK);
```

---

## Why this project is important

This project helped me understand:

* SPI communication in STM32
* Working with TFT displays
* Using DMA for faster data transfer
* Basic graphics rendering

This is an important step toward building:

* UI-based embedded systems
* dashboards
* IoT display interfaces
* graphical monitoring systems

---

## Limitations

* Only static text display
* No animations
* No touch input
* No dynamic data

---

## Future improvements

* Display sensor data on TFT
* Add animations or graphics
* Use touch-enabled display
* Build UI menus
* Integrate with ADC/UART projects

---

## Final note

This project was my first step into **embedded graphics systems**.

After this, I can build more advanced applications like:

* real-time data dashboards
* smart device interfaces
* graphical monitoring systems

---
