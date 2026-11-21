# AVR ATmega2560 & Programmable Logic Exam Guide

[![Live Demo](https://img.shields.io/badge/Live-GitHub%20Pages-brightgreen?style=for-the-badge&logo=github)](https://remonsaha-lab.github.io/microcontroller-guide-app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

An in-depth, interactive web application and study portal for **AVR ATmega2560 microcontrollers**, **Embedded Systems**, and **Programmable Logic (PLA / PAL / CPLD / FPGA)** course curricula and exam preparation.

---

## 🌐 Live Deployment

Access the live application hosted via GitHub Pages:

- **Master Knowledge & Exam Portal**: [https://remonsaha-lab.github.io/microcontroller-guide-app/](https://remonsaha-lab.github.io/microcontroller-guide-app/)
- **Interactive Circuit Laboratory**: [https://remonsaha-lab.github.io/microcontroller-guide-app/circuits.html](https://remonsaha-lab.github.io/microcontroller-guide-app/circuits.html)

---

## 🚀 Key Features

### 1. In-Depth Architectural Lectures
- **AVR Architecture Fundamentals**: Harvard architecture vs. Von Neumann, 16-bit / 32-bit pipelined execution stages, 32 general-purpose working registers ($R_0 - R_{31}$), and register pair pointers ($X, Y, Z$).
- **Memory Map & Addressing Modes**: Flash Program Memory, SRAM Data Memory, EEPROM, and I/O Memory registers. Direct, indirect with displacement, and pre-decrement/post-increment addressing modes.
- **Interrupts & Vectors**: Complete vector table prioritization, SREG global interrupt enable (`sei()` / `cli()`), and nested interrupt handling.
- **Timers & Counters**: 8-bit (Timer 0, Timer 2) and 16-bit (Timer 1, 3, 4, 5) peripherals operating in Normal, CTC (Clear Timer on Compare Match), Fast PWM, and Phase Correct PWM modes.
- **Serial Communication**: USART baud rate generation ($UBRR$), SPI master/slave shift registers, and TWI/I2C protocols.
- **Analog Peripherals**: 10-bit Successive Approximation ADC with selectable reference voltages ($AREF, AVCC, 1.1V, 2.56V$), prescalers ($2$ to $128$), and differential input channels.

### 2. Interactive Calculation & Synthesis Engines
- **Timer Normal Mode Preload Calculator**: Instant calculation of initial counter preload values (`TCNTn`) given target oscillator frequency ($f_{osc}$), prescaler factor ($N$), and desired delay duration ($t_{delay}$).
- **Full-Adder PLA / ROM Matrix Synthesizer**: Interactive diode AND matrix and transistor OR matrix configuration showing fuse programming and minterm selection for arithmetic functions.

### 3. Solved Exam Papers & Question Bank
- Comprehensive solutions to past semester exam questions with rigorous mathematical derivations.
- Register-level C code examples (AVR-GCC) and assembly language routines.
- Step-by-step schematics and pin connection references for the Arduino Mega 2560 board.

### 4. Interactive Circuit Laboratory (10 Hardware Models)
The dedicated [Circuit Laboratory](https://remonsaha-lab.github.io/microcontroller-guide-app/circuits.html) provides interactive, real-time simulated circuit models:
1. **Transistor-Buffered High-Current LED Driver**: NPN BC547 low-side switch protecting microcontroller I/O pins.
2. **Active-Low Digital Switch & Internal Pull-Up Resistor**: Door alarm monitoring circuit with switch bounce handling.
3. **Full-Adder Diode AND Matrix & Transistor OR Matrix**: Programmable Logic Array (PLA) physical circuit realization.
4. **6T CMOS Static RAM (SRAM) Memory Cell**: Cross-coupled bistable inverter latch with word line and bit lines ($BL / \overline{BL}$).
5. **10-Bit Successive Approximation Register (SAR) ADC**: Sample & Hold circuit, binary search DAC comparator loop, and conversion cycles.
6. **R-2R Resistor Ladder 4-Bit DAC with Buffer**: Precision binary-weighted resistor network with rail-to-rail operational amplifier follower.
7. **HD44780 16x2 Dot-Matrix Character LCD Interfacing**: 4-bit bus mode timing, nibble transfers, and command/data register selection ($RS, E, D_4 - D_7$).
8. **Watchdog Timer (WDT) & Power Architecture**: System reset timeouts, interrupt-before-reset modes, and Sleep modes (Idle, ADC Noise Reduction, Power-down).
9. **FPGA CMOS Transmission Gate vs. Pass-Transistor**: Complementary PMOS/NMOS transmission gate performance vs. single NMOS threshold voltage drop ($V_{DD} - V_{th}$).
10. **Dual Independent LED Blink & Hardware Pulse Counter**: Timer 3 in CTC mode combined with external pin $T_5$ pulse counting.

---

## 🛠️ Technology Stack

- **HTML5 & Semantic Markup**: Accessible and search-engine optimized structural layout.
- **Tailwind CSS**: Utility-first styling with custom palette inspired by clean editorial design (light / dark mode support).
- **KaTeX**: Fast, high-fidelity LaTeX mathematical typesetting for formulas and derivations.
- **Prism.js**: Code syntax highlighting for C and AVR Assembly.
- **Vanilla JavaScript**: Zero-dependency client-side interactivity, state management, and real-time calculation logic.

---

## 💻 Local Exploration

To run or review the guide locally, simply clone the repository and open `index.html` in any modern web browser:

```bash
git clone https://github.com/Remonsaha-lab/microcontroller-guide-app.git
cd microcontroller-guide-app
# Open in browser:
start index.html       # Windows
open index.html        # macOS
xdg-open index.html    # Linux
```

No build tools, Node.js, or package managers are required.

---

## 📄 License

This educational portal is released under the [MIT License](LICENSE).
