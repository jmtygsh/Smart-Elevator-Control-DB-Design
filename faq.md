# FAQ

## How many buildings are connected to the platform?

Yes. Using the `building` table.

---

## How many elevators exist inside a building?

Yes. Using the `elevators` table filtered by `building_id`.

---

## Which floors belong to which building?

Yes. Using the `floors` table linked by `building_id`.

---

## Which elevator serves which floors?

Yes. Using the `elevator_floor` mapping table.

---

## What requests were generated from which floors?

Yes. Using the `floor_requests` table linked by `floor_id`.

---

## Which elevator handled a request?

Yes. Using the `ride_assignment` table.

---

## Can multiple elevators serve the same floor?

Yes. Through the `elevator_floor` table.

---

## Can one elevator serve multiple floors?

Yes. Through the `elevator_floor` table.

---

## What is the status of each elevator (idle, moving, maintenance)?

Yes. Using `elevators.status`.

---

## How many rides did an elevator complete today?

Yes. Using the `ride_logs` table.

---

## Which elevator handled the most requests?

Yes. Using `ride_assignment` or `ride_logs`.

---

## Which requests are still pending?

Yes. Using `floor_requests.status = pending`.

---

## Can an elevator be temporarily disabled for maintenance?

Yes. Using `elevators.is_active = false`.

---

## Can maintenance history be tracked per elevator?

Yes. Using the `maintenance_tracking` table.

---

## Can ride logs be recorded for analytics later?

Yes. Using the `ride_logs` table.
