# AutoBench

AutoBench is an STM32F407-based automotive-style motor control test bench focused on closed-loop speed control, telemetry, fault handling, and measured validation.

## Current Milestone

v0.5 Open-Loop Motor Telemetry

## Project Goal

The goal of this project is to build a student-scale embedded control bench using STM32F407G-DISC1.

The first working version will demonstrate:

- PWM motor driving
- Encoder-based RPM measurement
- UART telemetry
- Python live plotting
- Open-loop step response measurement
- Measured validation with logs and plots

Later versions will add:

- PID speed control
- Fault handling
- CAN loopback
- Automotive-style state machine
- ACC-inspired control scenario
- Automated Python tests

## Hardware Platform

- STM32F407G-DISC1
- STM32CubeIDE
- Embedded C firmware
- Python tools for logging, plotting, and validation

## Repository Structure

| Folder | Purpose |
|---|---|
| docs/ | Technical notes and documentation |
| firmware/ | STM32 firmware project |
| tools/ | Python logging and plotting tools |
| results/ | CSV logs, plots, and test results |
| media/ | Demo videos, screenshots, and GIFs |

## Milestones

- v0.5 Open-Loop Motor Telemetry
- v1.0 PID Motor Control MVP
- v2.0 Automotive Showcase
- v3.0 Final AutoBench
