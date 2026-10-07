# Task 2 — Formalize Constraints

## Formal Expressions

|Const-ID | Formal expression |
|----|-------------------|
| C1 | Train_In_Crossing → ¬Barrier_Open |
| C2 | (Train_Approaching ∨ Train_In_Crossing) → (Lights_On ∧ Alarm_On) |
| C3 | Train_In_Crossing → Barrier_Closed |
| C4 | Barrier_Opening → (Train_Cleared ∧ ¬Train_In_Crossing) |
| C5 | ¬Barrier_Open → Road_Signal_Red |
| C6 | Sensor_Fault → (Barrier_Closed ∧ Alarm_On ∧ Control_Center_Alerted) |
| C7 | Sensor_Conflict → ¬Train_Cleared |
| C8 | Emergency → (Barrier_Closed ∧ Road_Signal_Red ∧ Control_Center_Alerted) |
