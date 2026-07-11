# RoutePilot MVP v1.0

## Product promise

RoutePilot helps delivery drivers finish routes faster by combining route organization, map-based clustering, shared location intelligence, opportunistic delivery, and live progress tracking.

## Locked MVP scope

### 1. Route dashboard

Show:

- Route date
- Package count
- Unique stop count
- Completed and remaining packages
- Start time
- Starting mileage
- Current mileage
- Estimated finish time
- Apartments, gated communities, businesses, and houses
- Stops requiring access assistance
- Weather risk flag

### 2. Route map

- Plot every unique delivery location.
- Keep every pending stop visible as an active, tappable marker.
- Group nearby stops into clusters.
- Use one marker for multiple packages at the same address.
- Show stop status on the map.
- Show the driver's current GPS location.
- Highlight stops near the driver's current position.
- Allow opening any selected stop in Apple Maps.
- Visually distinguish completed, skipped, retry-later, priority, apartment, gated, and business stops.

### 3. Opportunistic Delivery Mode

Drivers must be able to complete a convenient nearby stop without losing the original optimized route.

Required behavior:

- Show a live `Nearby Stops` list ordered by distance from the driver.
- Display stop number, distance, package count, stop type, priority, and access warning.
- Let the driver tap any pending map marker or nearby-stop card.
- Offer `Deliver Now` or `Stay on Optimized Route`.
- Warn when taking the nearby stop is likely to create meaningful backtracking.
- Preserve the original optimized sequence for all remaining stops.
- After an out-of-order completion, remove that stop from the pending route and recalculate the remaining ETA and sequence.
- Never auto-switch stops while the vehicle is moving; the driver must select the stop while safely parked.

Example nearby-stop card:

- Stop 673
- 0.1 miles away
- 2 packages
- Apartment
- Gate access required
- Estimated detour impact: +0 minutes

### 4. Stop detail

Store:

- Shipment number
- Recipient
- Full address
- Apartment or unit
- Telephone number
- Gate or call-box code
- Building name
- Business hours
- Parking instructions
- Entrance instructions
- Elevator or stair notes
- Delivery priority
- Recommended time window
- Driver notes
- Shared location notes

### 5. Stop statuses

- Pending
- In progress
- Completed
- Retry later
- Undeliverable

### 6. Route intelligence

Flags:

- Apartment
- Gated community
- Business
- Mobile-home park
- Multi-package address
- Access problem
- Closing soon
- Prioritize early
- Do last
- Weather-sensitive
- Nearby opportunity
- Backtracking risk

### 7. Driver workflow

1. Import route.
2. Confirm route totals.
3. Enter start time and starting mileage.
4. Review clusters and critical stops.
5. Start the recommended first cluster.
6. Keep all remaining stops active on the live map.
7. Follow the optimized route or select a nearby opportunity while safely parked.
8. Complete stops and capture notes.
9. Recalculate remaining ETA and sequence after completed, skipped, or out-of-order stops.
10. Enter ending mileage and finish time.

## Deferred until after field testing

- Dispatcher portal
- Payroll
- Fleet maintenance
- Billing
- Enterprise analytics
- Public driver marketplace
- Full automated screenshot OCR

## First validation target

Use RoutePilot on one real route and confirm that it can:

- represent the full package count,
- prevent duplicate-address errors,
- make route order easier to follow,
- keep every pending stop available as an active map link,
- support safe out-of-order nearby deliveries without losing route logic,
- preserve access information,
- and produce a reliable completion estimate.
