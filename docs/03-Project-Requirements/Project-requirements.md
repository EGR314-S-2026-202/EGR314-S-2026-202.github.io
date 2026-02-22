---
title: Project Requirements
---

## Requirements Table

| Requirement ID | Requirement Description | Minimum (Not Failure) | Target Measurement | Feature Satisfied | Stretch Goal? (Y/N) / Possible Stretch Goals |
|---|---|---|---|---|---|
| TR-01 | Rover shall be remotely driven forward, reverse, and turn | Forward and Backward | Turning left and right | Actuator | **No** |
| TR-02 | The system shall operate on battery power | ≥ 10 min runtime and power all systems | ≥ 30 min runtime | Power | **No** |
| TR-03 | Rover shall measure soil or environmental humidity | Wet/Dry | High Resolution | Sensor | **No** |
| TR-04 | Rover shall be controlled through a human-machine interface | Buttons only | Button + display | HMI | **No** |
| TR-05 | Rover shall measure the ambient temperature | 土 5 ℃ | 土 2 ℃ | Sensor | **No** <br> <br> Be able to convert C to F |
| TR-06 | Rover shall send sensor data to the controller screen and get control information back | Inputs make the rover move/get sensor data | Low Latency / Clean data and graphs | Communication | **No** <br> <br> Store data in a .csv convertible data bank |
| TR-07 | All individual boards talk to each other using the same communication lines | One-way messages | Two-way UART messaging | HMI | **No** |
| TR-08 | Rover will protect probes from being destroyed using pressure sensing. | At any pressure, the arm stops and returns home | At a specified pressure arm returns home and sends an error message | Sensor / Controller | **No** |
| TR-09 | Subsystems will send error reports to HMI | Alive signals | Specific issues with possible solutions given | Communication | **No** |
| TR-10 | Rover shall initialize all subsystems and indicate when the system is ready for operation | Power-on and basic communication | All subsystems report ready to HMI within 10 seconds | System integration / HMI | **No** |



## Team Member Subsystem Assignment

| Team Member | Subsystem Responsibility | Primary Requirements |
|---|---|---|
| Jacob Alger | Human-Machine Interface | TR-03, TR-07, TR-10, supports TR-06 |
| Tyler Dean | Rover sensors (Pressure/Tilt) | Sensor: TR-06, TR-07, TR-08 |
| Cristopher Gutierrez | Wireless Communication | TR-06, TR-09 |
| Isaiah Johnston | Environmental Sensors (Temp/Humidity) | TR-03, TR-05 |
| Aaron Kiem | Metal Detector Subsystem | TR-06, TR-09 |
| Asadbek Ruziev | Wheel motor subsystem | TR-01 |
| Caleb Yuen | Front Arm Subsystem | TR-08, supports TR-01 (actuation) |


## Requirement Explanations
- **TR-01:**  
  This requirement ensures the rover can be remotely driven forward, backward, and turned by the user. Since the goal of CropScout is to explore agricultural fields without requiring the user to walk through them, basic mobility is essential. Forward and backward motion allows the rover to navigate rows, while turning enables it to avoid obstacles and reposition itself. This requirement supports all other system functions by allowing the rover to reach areas of interest.

- **TR-02:**  
  CropScout is intended to operate in outdoor field environments where access to wall power is not available. Because of this, the system must run entirely on battery power for a reasonable amount of time. Establishing a minimum runtime ensures the rover can complete basic tasks, while a longer target runtime improves usability. This requirement also places constraints on subsystem power consumption and overall system design.

- **TR-03:**  
  Measuring soil or environmental humidity allows the rover to provide useful information related to crop and soil conditions. At a minimum, the rover should be able to distinguish between wet and dry conditions, which can help identify irrigation issues. Higher resolution measurements allow for more detailed analysis and better decision-making. This requirement supports CropScout’s role as a monitoring and inspection tool.

- **TR-04:**  
  A human-machine interface is required so the user can control the rover and interact with its data. At a minimum, physical buttons allow basic control of movement and system functions. Adding a display improves usability by providing feedback such as sensor readings, system status, and error messages. This requirement ensures the rover can be operated intuitively without relying on autonomous behavior.

- **TR-05:**  
  Ambient temperature is an important environmental parameter that can affect crop health and growing conditions. This requirement ensures the rover can measure temperature with reasonable accuracy instead of relying on estimates. Improving accuracy in the target measurement allows for more reliable data collection. Temperature data also complements other sensor readings to provide a more complete picture of field conditions.

- **TR-06:**  
  CropScout must be able to send sensor data to the controller while also receiving control commands from the user. This two-way communication allows the user to both monitor the environment and actively control the rover’s behavior. Low latency ensures that the rover responds quickly to user inputs and that sensor data appears in real time. This requirement is critical for smooth operation and user confidence in the system.

- **TR-07:**  
  Because CropScout is made up of multiple modular subsystems, all boards must communicate using the same communication lines. At a minimum, one-way messaging allows basic data transfer between subsystems. Two-way UART communication enables more advanced interactions, such as acknowledgments and status reporting. This requirement ensures the system functions as a unified device rather than a collection of independent boards.

- **TR-08:**  
  The front arm subsystem interacts directly with the environment, which introduces the risk of damaging probes or mechanical components. This requirement ensures that the system can detect excessive pressure and respond safely. When unsafe conditions are detected, the arm must stop and return to a safe position. Error reporting helps inform the user of what occurred and prevents repeated damage.

- **TR-09:**  
  Subsystem error reporting improves system reliability and helps users understand what is happening during operation. At a minimum, alive signals indicate that subsystems are still functioning. More detailed error messages allow users to identify specific problems and take corrective action. This requirement supports easier debugging and a better overall user experience.

- **TR-10:**  
  A clear startup and initialization process is necessary to ensure all subsystems are ready before operation begins. This requirement ensures that basic communication is established as soon as the system powers on. Reporting readiness to the HMI within a defined time gives the user confidence that the rover is functioning properly. This also helps prevent commands from being sent before the system is fully initialized.

