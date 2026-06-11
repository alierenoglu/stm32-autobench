# Pinout

This document tracks STM32F407G-DISC1 pin assignments for AutoBench.

## Current Pin Plan

| Function | Pin | Peripheral | Notes |
|---|---|---|---|
| Status LED Green | PD12 | GPIO | System alive |
| Status LED Orange | PD13 | GPIO | Warning |
| Status LED Red | PD14 | GPIO | Fault |
| Status LED Blue | PD15 | GPIO | Active |
| User Button | PA0 | GPIO / EXTI | Enable or mode button |
| Motor PWM | PA8 | TIM1_CH1 | Planned for TB6612FNG PWMA |
| Motor Direction 1 | PE7 | GPIO | Planned for TB6612FNG AIN1 |
| Motor Direction 2 | PE8 | GPIO | Planned for TB6612FNG AIN2 |
| UART TX | PA2 | USART2_TX | Planned telemetry to CP2102 RX |
| UART RX | PA3 | USART2_RX | Planned telemetry from CP2102 TX |
| Potentiometer | PC1 | ADC1_IN11 | Planned speed command input |
| Encoder A | PB4 | TIM3_CH1 | Planned quadrature encoder input |
| Encoder B | PB5 | TIM3_CH2 | Planned quadrature encoder input |
| CAN RX | PD0 | CAN1_RX | Planned for v2.0 / v3.0 |
| CAN TX | PD1 | CAN1_TX | Planned for v2.0 / v3.0 |

## Notes

- Motor power must come from an external 5V supply.
- STM32 GND, motor driver GND, and USB-UART GND must be connected together.
- PB4 may conflict with JTAG. Use Serial Wire debug mode if TIM3 encoder mode causes issues.
- CAN is not required for v0.5.
