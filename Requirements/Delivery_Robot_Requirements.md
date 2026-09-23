# Delivery Robot Requirements

| Req. ID | Requirement |
|---|---|
| R1 | The robot shall remain in IDLE when it is powered on and no delivery request is available. |
| R2 | The robot shall transition from IDLE to NAVIGATING only after receiving a valid delivery request. |
| R3 | The robot shall navigate toward the requested destination while in the NAVIGATING state. |
| R4 | The robot shall enter AVOIDING_OBSTACLE when an obstacle is detected during navigation. |
| R5 | The robot shall return from AVOIDING_OBSTACLE to NAVIGATING after the obstacle has been successfully avoided. |
| R6 | The robot shall enter DELIVERING only after it reaches the destination while navigating normally. |
| R7 | The robot shall not enter DELIVERING directly from IDLE or AVOIDING_OBSTACLE. |
| R8 | The robot shall return to the warehouse after successfully completing the delivery. |
| R9 | The robot shall stop its current delivery journey and enter RETURNING when its battery reaches a critical level during navigation. |
| R10 | The robot shall transition from RETURNING to IDLE after reaching the warehouse. |
