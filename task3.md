# Task 3 — Identify Constraint Violations

### V1
**Constraint (C1):** `Train_In_Crossing → ¬Barrier_Open`
**Violation:** `Train_In_Crossing = TRUE`, `Barrier_Open = TRUE`
**Explanation:** The barrier is open while a train is on the crossing. The premise is TRUE but `¬Barrier_Open` is FALSE, so the rule is broken.

### V2
**Constraint (C2):** `(Train_Approaching ∨ Train_In_Crossing) → (Lights_On ∧ Alarm_On)`
**Violation:** `Train_Approaching = TRUE`, `Lights_On = TRUE`, `Alarm_On = FALSE`
**Explanation:** A train is approaching but the alarm is silent. `Lights_On ∧ Alarm_On` is FALSE because `Alarm_On` is FALSE.

### V3
**Constraint (C3):** `Train_In_Crossing → Barrier_Closed`
**Violation:** `Train_In_Crossing = TRUE`, `Barrier_Open = FALSE`, `Barrier_Closed = FALSE`
**Explanation:** The barrier is stuck halfway while the train is on the crossing. `Barrier_Closed` is FALSE, so the rule is broken.

### V4
**Constraint (C4):** `Barrier_Opening → (Train_Cleared ∧ ¬Train_In_Crossing)`
**Violation:** `Barrier_Opening = TRUE`, `Train_Cleared = FALSE`
**Explanation:** The barrier started opening before the train was confirmed clear. `Train_Cleared` is FALSE, so the conclusion is FALSE.

### V5
**Constraint (C5):** `¬Barrier_Open → Road_Signal_Red`
**Violation:** `Barrier_Closed = TRUE`, `Barrier_Open = FALSE`, `Road_Signal_Red = FALSE`
**Explanation:** The barrier is closed but the road signal is not red. The premise is TRUE and `Road_Signal_Red` is FALSE.

### V6
**Constraint (C6):** `Sensor_Fault → (Barrier_Closed ∧ Alarm_On ∧ Control_Center_Alerted)`
**Violation:** `Sensor_Fault = TRUE`, `Barrier_Open = TRUE`, `Alarm_On = FALSE`, `Control_Center_Alerted = FALSE`
**Explanation:** A sensor failed but the system stayed in normal mode. None of the required fail-safe actions happened.

### V7
**Constraint (C7):** `Barrier_Fault → (Control_Center_Alerted ∧ Road_Signal_Red)`
**Violation:** `Barrier_Fault = TRUE`, `Road_Signal_Red = TRUE`, `Control_Center_Alerted = FALSE`
**Explanation:** The barrier failed and traffic is stopped, but nobody was notified. `Control_Center_Alerted` is FALSE.

### V8
**Constraint (C8):** `Comm_Loss → (Barrier_Closed ∧ Alarm_On)`
**Violation:** `Comm_Loss = TRUE`, `Barrier_Open = TRUE`, `Barrier_Closed = FALSE`, `Alarm_On = FALSE`
**Explanation:** Communication was lost but the crossing stayed open and silent instead of going fail-safe.
