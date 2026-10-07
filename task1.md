# Task 1 — Identify Constraints

| Const-ID | Constraint | Why it is necessary |
|----|-----------------------------|---------------------|
| C1 | The barrier must not be open while a train is in the crossing. | Opening lets road vehicles enter while the train passes, causing a collision. |
| C2 | Warning lights and the audible alarm must be ON whenever a train is approaching or in the crossing. | Drivers and pedestrians must be warned before and during train passage. |
| C3 | The barrier must be fully closed while a train is in the crossing. | A half-closed or moving barrier leaves a gap that vehicles can pass through. |
| C4 | The barrier may start opening only after the train has been confirmed as completely cleared and no train is in the crossing. | Prevents early opening while part of the train is still on the crossing. |
| C5 | The road traffic signal must be RED whenever the barrier is not fully open. | Stops road traffic from approaching a closed or moving barrier. |
| C6 | If a sensor failure is detected, the system must close the barrier, sound the alarm and alert the control center. | A blind system cannot know if a train is coming, so it must default to the safe state. |
| C7 | If a barrier failure is detected, the control center must be alerted and the road signal set to RED. | Traffic must be stopped and operators informed when the barrier cannot be trusted. |
| C8 | If communication with the control center is lost, the system must keep the barrier closed and the alarm active (fail-safe). | Without communication, the system cannot be supervised, so it must choose the safest state. |
| C9 | If sensor readings conflict, the crossing must not be treated as cleared. | Incorrect/inconsistent data must never lead to the barrier opening. |
| C10 | In an emergency condition, the barrier must be closed, the road signal RED and the control center alerted. | Emergencies need immediate protection of road users and operator awareness. |
