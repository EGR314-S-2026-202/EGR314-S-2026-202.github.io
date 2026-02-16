---
title: Block Diagram, Protocol, and Message Structure
---

## Team Block Diagram

Add content!
> **Note:** You can download the Team Block Diagram as a PNG [here]

## Communication Process Diagram

Add content!

## Message Types

| Sending                | Receiving       | Message Data Type | Message      | Notes/Details                                           |
| ---------------------- | --------------- | ----------------- | ------------ | ------------------------------------------------------- |
| Wireless Communication | HMI             | digital           | BT_STATUS    | 1 = Connected <br> 0 = Disconnected                     |
| Temp                   | HMI             | string            | “X℃/℉”      | N/A                                                     |
| Humidity               | HMI             | string            | “X% RH”      | N/A                                                     |
| Accelerometer          | Front Arm       | digital           | “1” or “0”   | 1 for safe to continue 0 to indicate object impact      |
| HMI / Wireless         | Front Arm       | int               | SET_POSITION | Used to rotate base stepper motor to specified position |
| Front Arm              | HMI / Wireless  | int               | ACK_POSITION | Sent after motion completes to confirm position reached |
| Front Arm              | HMI             | string            | ARM_STATUS   | Indicates current state of actuator                     |
| Front Arm              | HMI / Wireless  | int               | ARM_ERROR    | 0 = No Error, 1 = Stall, 2 = Overcurrent, etc.          |
| HMI                    | Front Arm       | digital           | JOG_ENABLE   | 1 = Move, 0 = Stop                                      |
| HMI                    | Wheels          | 2-bit int         | 11           | Forward                                                 |
| HMI                    | Wheels          | 2-bit int         | 00           | Backward                                                |
| HMI                    | Wheels          | 2-bit int         | 01           | Right                                                   |
| HMI                    | Wheels          | 2-bit int         | 10           | Left                                                    |
| HMI                    | Temp            | digital           | 1            | 1 = Send reading <br> 0 = Nothing                       |
| HMI                    | Humidity        | digital           | 1            | 1 = Send reading <br> 0 = Nothing                       |
| HMI                    | Accelerometer   | digital           | 1            | 1 = Send reading <br> 0 = Nothing                       |
| HMI                    | Pressure Sensor | digital           | 1            | 1 = Send reading <br> 0 = Nothing                       |
| HMI                    | Metal Detector  | digital           | 1            | 1 = Send reading <br> 0 = Nothing                       |

