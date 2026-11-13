# Use Case Specifications

## 1. Smart Parking & Access Control Module
- **UC01 — Consult Real-Time Availability:** Allows authenticated users to query available slots per zone (`Parque A`, `B`, `C`, `D`) and slot type (`Covered`, `EV Charging`, `Reduced Mobility`).
- **UC02 — Reserve Parking Slot:** Validates user role permissions (`Dirigente`, `Professor Visitante`), checks slot availability for the target date/time window, and registers the reservation.
- **UC03 — Authenticate & Enter Campus (`RFID` / `QR Code` / `LPR`):** Reads vehicle license plate or RFID/QR credential at the barrier, validates active permissions or approved reservations, and logs the entry event.
- **UC04 — Manage Permissions & Infractions:** Synchronizes academic/HR profiles, configures zone rules, and records unauthorized parking penalties.

## 2. Billing & Invoicing Module (`ex fatura`)
- **UC05 — Issue & Settle Invoice:** Tracks invoice issuance, partial installment payments (`valor < divida`), debt recalculation, and receipt emission.
