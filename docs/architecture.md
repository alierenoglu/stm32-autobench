# Architecture

AutoBench is organized as a small embedded control system with three main parts:

1. STM32 firmware
2. Python PC tools
3. Measured results and documentation

## System Overview

STM32F407G-DISC1 controls a DC motor using PWM.

The motor speed is measured with a quadrature encoder.

The STM32 sends telemetry to the PC over UART.

Python tools read telemetry, save CSV logs, draw live plots, and calculate metrics.

## Data Flow

User input or test command  
→ STM32 control firmware  
→ PWM motor output  
→ encoder speed feedback  
→ UART telemetry  
→ Python logger and plotter  
→ results folder

## Firmware Layers

| Layer | Purpose |
|---|---|
| app/ | Control logic such as PID, state machine, and fault handling |
| service/ | Telemetry, protocol handling, and future CAN message logic |
| driver/ | Hardware access such as GPIO, PWM, encoder, ADC, UART, and watchdog |

## PC Tools

| Tool | Purpose |
|---|---|
| logger.py | Reads UART telemetry and saves CSV logs |
| live_plot.py | Shows real-time telemetry graphs |
| metrics.py | Calculates overshoot, settling time, steady-state error, and fault response time |

## v0.5 Architecture

v0.5 focuses on open-loop motor telemetry:

- PWM motor command
- encoder RPM measurement
- UART telemetry
- Python live plotting
- open-loop step response logging

PID, CAN, watchdog, and ACC-inspired scenarios are planned for later milestones.
