# LED Blink Result

## Goal

Configure PD12 as GPIO output and blink the onboard green LED on the STM32F407G-DISC1 board.

## GPIO Configuration

PD12 was configured as GPIO output in STM32CubeIDE.

PD12 settings:

- Port: GPIOD
- Pin: GPIO_PIN_12
- Mode: GPIO_MODE_OUTPUT_PP
- Pull: GPIO_NOPULL
- Speed: GPIO_SPEED_FREQ_LOW

## Blink Code

The following code was added inside the main loop:

```c
HAL_GPIO_TogglePin(GPIOD, GPIO_PIN_12);
HAL_Delay(500);
```
## Test

The firmware was built successfully with:

- 0 errors

- 0 warnings

The firmware was flashed to the STM32F407G-DISC1 board using STM32CubeIDE.

## Result

The onboard green LED connected to PD12 blinks successfully.

Blink timing:

- 500 ms ON

- 500 ms OFF

