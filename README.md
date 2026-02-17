# 555 Timer Clock Module for Breadboard CPUs

## Overview
This project is a discrete hardware clock module built around the LM555 timer in astable mode.  
It generates a stable square-wave clock signal for breadboard-based digital systems such as 8-bit CPUs and microprocessor prototypes.

The module provides adjustable clock speeds, enabling both continuous operation and slow, controlled stepping for debugging and verification of processor behavior.

## Features
- 555 timer configured as an astable multivibrator
- Adjustable clock frequency via potentiometer
- Clean square-wave output for TTL-compatible logic
- Wide speed range:
  - Slow clock for step-through debugging
  - Higher-speed clock for normal operation
- Breadboard-friendly design
- Designed for integration with custom 8-bit CPU / microprocessor systems

## Why This Exists
When developing a breadboard CPU, a reliable clock is critical.  
This module allows:
- Instruction-level debugging at human-visible speeds
- Stable timing for memory and control logic
- Repeatable testing across different subsystems

It eliminates the need for external lab signal generators and keeps the entire system self-contained.

## How It Works
The LM555 is configured in astable mode:

f ≈ 1 / (0.693 × (R1 + 2R2) × C)

A potentiometer is used to vary the charge/discharge time of the timing capacitor, which adjusts the output frequency.

The output is a square wave suitable for driving:
- 74xx / 74LS / 74HC logic
- Program counters
- Registers
- Control logic
- EEPROM-based systems

## Hardware
### Core Components
- LM555 timer
- Timing capacitor
- Fixed resistors
- Potentiometer (frequency control)
- Decoupling capacitor
- Output header

### Output
- TTL-compatible square wave clock signal

## Use Cases
- Breadboard 8-bit CPU clock source
- Microprocessor system bring-up
- Step-through debugging of instruction cycles
- Control signal timing verification
- Educational digital logic projects

## Integration
This module is designed to plug directly into a breadboard system and drive the system clock line.

## Future Improvements
- Push-button manual clock (single-step mode)
- Clock enable / halt control
- Buffered output stage
- LED frequency indicator
- PCB version

## Author
Cris R. Martinez Hernandez
Electrical Engineering @ University of Washington Bothell

## License
MIT
