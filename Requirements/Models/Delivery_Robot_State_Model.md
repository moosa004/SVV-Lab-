# Delivery Robot State Model

## States

### S1 — IDLE
The robot is waiting for a delivery request.

### S2 — NAVIGATING
The robot is moving toward the destination.

### S3 — AVOIDING_OBSTACLE
The robot is temporarily dealing with an obstacle.

### S4 — DELIVERING
The robot is delivering the package at the destination.

### S5 — RETURNING
The robot is returning to the warehouse.

## Events / Conditions

- E1 — Delivery Request Received
- E2 — Destination Reached
- E3 — Obstacle Detected
- E4 — Obstacle Avoided
- E5 — Delivery Successful
- E6 — Warehouse Reached
- E7 — Critical Battery
