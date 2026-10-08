# Microcontroller-Lab02: Timer Interrupt and LED Scanning

## Course Information

**Course:** Microprocessors-Microcontrollers (CO3009)  
**Laboratory:** Lab 02 - Timer Interrupt and LED Scanning

## Overview

This repository contains the implementation of Lab 02 for the
Microprocessors-Microcontrollers course.

The projects are developed using the **STM32F103C6 microcontroller**,
**STM32CubeIDE**, and **Proteus**.

The laboratory focuses on timer interrupts, seven-segment display scanning,
software timers, non-blocking timing, digital clock implementation, and
8-by-8 LED matrix control.

## Objectives

The main objectives are:

- Configure TIM2 to generate a periodic interrupt.
- Implement multiplexed seven-segment display scanning.
- Develop reusable display-update functions.
- Implement software timers based on timer interrupts.
- Replace blocking delays with non-blocking timing.
- Build a digital clock using four seven-segment displays.
- Control and animate an 8-by-8 LED matrix.

## Laboratory Exercises

### Exercise 1: Two Seven-Segment Displays

Control two common-anode seven-segment displays and alternately display
digits 1 and 2 with a switching time of 500 ms.

### Exercise 2: Four Seven-Segment Displays

Extend the system to four seven-segment displays. Display 1, 2, 3, and 0,
while blinking the DOT LEDs every second.

### Exercise 3: `update7SEG()` Function

Implement the `update7SEG(int index)` function to select one display and
show the corresponding value from `led_buffer`.

### Exercise 4: 1 Hz Display Scanning

Adjust the display-switching period so that one complete scan of four
seven-segment displays has a frequency of 1 Hz.

### Exercise 5: Digital Clock

Implement a digital clock displaying hour and minute in HH:MM format.
The `updateClockBuffer()` function converts time values into four display
digits.

### Exercise 6: Software Timer

Implement a software timer based on the 10 ms TIM2 interrupt and use timer
flags for non-blocking timing.

### Exercise 7: Non-Blocking Digital Clock

Replace `HAL_Delay()` with a software timer. Update the clock and DOT LED
from the main loop.

### Exercise 8: Main-Loop Display Scanning

Move `update7SEG()` from the timer interrupt to the main loop. The interrupt
handler is reduced to software-timer processing only.

### Exercise 9: 8-by-8 LED Matrix

Add an 8-by-8 LED matrix controlled through a ULN2803 transistor array.
Implement `updateLEDMatrix()` and display the character A.

### Exercise 10: LED-Matrix Animation

Create a simple LED-matrix animation by cyclically shifting the matrix
bitmap while continuing periodic matrix scanning.

## Timer Configuration

TIM2 uses the internal 8 MHz clock with:

- Prescaler: `7999`
- Counter period: `9`
- Timer interrupt period: `10 ms`
- Timer interrupt frequency: `100 Hz`

## Development Environment

### Hardware

- STM32F103C6 Microcontroller
- Common-anode seven-segment displays
- 8-by-8 LED matrix
- ULN2803 transistor array
- LEDs and PNP transistors

### Software Tools

- STM32CubeIDE
- Proteus Simulation Software
- STM32 HAL Library

## Repository Structure

```text
Microcontroller-Lab02
│
├── Proteus
│   ├── Exercise1.pdsprj
│   ├── Exercise2-8.pdsprj
│   └── Exercise9-10.pdsprj
│
├── STM32
│   ├── Exercise1
│   ├── Exercise2
│   ├── Exercise3
│   ├── Exercise4
│   ├── Exercise5
│   ├── Exercise6
│   ├── Exercise7
│   ├── Exercise8
│   ├── Exercise9
│   └── Exercise10
│
├── README.md
└── .gitignore
```
## Key Concepts

- Timer interrupt
- LED scanning
- Seven-segment multiplexing
- Software timer
- Non-blocking timing
- Digital clock
- LED matrix scanning
- LED matrix animation

## Simulation

All circuits are designed and tested using Proteus.

The repository includes:

- STM32CubeIDE source code
- Proteus schematic files
- Seven-segment display experiments
- Digital clock implementation
- LED matrix display and animation

## Author

**Le Hien Vinh**
