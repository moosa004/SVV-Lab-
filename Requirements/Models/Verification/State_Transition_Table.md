# State Transition Table

| Current State | Event / Condition | Next State | Requirement |
|---|---|---|---|
| IDLE | Delivery Request Received | NAVIGATING | R2 |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE | R4 |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING | R5 |
| NAVIGATING | Destination Reached | DELIVERING | R6 |
| DELIVERING | Delivery Successful | RETURNING | R8 |
| NAVIGATING | Critical Battery | RETURNING | R9 |
| RETURNING | Warehouse Reached | IDLE | R10 |

## Verification

### Check 1 — Invalid Transition

IDLE → DELIVERING

This transition must not be allowed because it violates R7.

The robot must first receive a delivery request and navigate toward the destination.

Correct:

IDLE → NAVIGATING → DELIVERING

### Check 2 — Missing Transition

NAVIGATING → AVOIDING_OBSTACLE

The robot must have a transition back:

AVOIDING_OBSTACLE → NAVIGATING

Otherwise, the robot would become stuck in obstacle-avoidance mode.

### Check 3 — Obstacle During Delivery

AVOIDING_OBSTACLE → DELIVERING

This transition must not be allowed because the robot must first return to NAVIGATING.

Correct:

AVOIDING_OBSTACLE → NAVIGATING → DELIVERING
