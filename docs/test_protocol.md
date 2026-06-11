# Test Protocol

All claims in AutoBench must be backed by logs, plots, screenshots, or videos.

## Measurement Rule

A feature is not considered complete unless it has at least one proof item:

- working firmware
- commit
- CSV log
- plot
- screenshot
- short video
- README or documentation update

## v0.5 Test Targets

| Test | Expected Result | Proof |
|---|---|---|
| LED blink test | PD12 blinks at a visible rate | Short video |
| Button test | PA0 changes system state | Short video or notes |
| PWM output test | Duty value changes from firmware | Code + test note |
| UART telemetry test | PC receives STM32 messages | Screenshot or log |
| Python logger test | Telemetry is saved to CSV | CSV file |
| Python live plot test | Telemetry appears on live graph | Screenshot |
| Open-loop motor test | Motor speed changes with duty | Short video |
| Encoder count test | Counter changes when motor turns | Log or screenshot |
| RPM calculation test | RPM increases with motor speed | CSV + plot |
| Open-loop step test | Duty step causes visible RPM response | CSV + plot |

## v0.5 Done Criteria

v0.5 is complete only if:

- motor runs open-loop
- encoder RPM is measured
- UART telemetry is received on PC
- Python live plot works
- open-loop step response is logged
- 60-second demo video exists
