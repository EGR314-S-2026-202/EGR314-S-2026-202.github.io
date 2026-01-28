---
title: Project Requirements
---

## Requirements Table

| Requirement ID | Requirement Description | Minimum (Not Failure) | Target Measurement | Feature Satisfied | Stretch Goal? (Y/N) | Possible Stretch Goals |
|---|---|---|---|---|---|---|
| TR-01 | Rover shall be remotely driven forward, reverse, and turn | Forward and Backward | Turning left and right | Actuator | No | |
| TR-02 | The system shall operate on battery power | ≥ 10 min runtime and power all systems | ≥ 30 min runtime | Power | No | |
| TR-03 | Rover shall measure soil or environmental humidity | Wet/Dry | High Resolution | Sensor | No | |
| TR-04 | Rover shall be controlled through a human-machine interface | Buttons only | Button + display | HMI | No | |
| TR-05 | Rover shall measure the ambient temperature | 土 5 ℃ | 土 2 ℃ | Sensor | No | Be able to convert C to F |
| TR-06 | Rover shall send sensor data to the controller screen and get control information back | Inputs make the rover move/get sensor data | Low Latency / Clean data and graphs | Communication | Np | Store data in a .csv convertible data bank |
| TR-07 | All individual boards talk to each other using the same communication lines | One-way messages | Two-way UART messaging | HMI | No | |
| TR-08 | Rover will protect probes from being destroyed using pressure sensing. | At any pressure, the arm stops and returns home | At a specified pressure arm returns home and sends an error message | Sensor / Controller | No | |
| TR-09 | Subsystems will send error reports to HMI | Alive signals | Specific issues with possible solutions given | Communication | No | |
| TR-10 | Rover shall initialize all subsystems and indicate when the system is ready for operation | Power-on and basic communication | All subsystems report ready to HMI within 10 seconds | System integration / HMI | No | |
| TR-11 | Rover shall deploy a physical marker using the front arm subsystem. | Rover shall deploy a physical marker using the front arm subsystem. | Can select and deploy one of multiple marker types | Actuator | No | |


## Team Member Subsystem Assignment


## Requirement Explanations
- **TR-01:** ...
- **TR-02:** ...
- **TR-03:** ...
- **TR-04:** ...
- **TR-05:** ...
- **TR-06:** ...
- **TR-07:** ...
- **TR-08:** ...
- **TR-09:** ...
- **TR-10:** ...
- **TR-11:** ...

