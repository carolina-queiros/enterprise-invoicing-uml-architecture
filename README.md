# Enterprise Invoicing & Access Control — UML Architecture

Object-oriented systems analysis, requirements engineering, and UML 2.5 architectural modeling (Visual Paradigm CASE) covering enterprise billing lifecycles and smart campus access/parking management.

## Repository Structure

- **[01-use-case-specifications](./01-use-case-specifications)** — Functional requirements, actor boundaries (`Administrator`, `BillingOperator`, `FacultyMember`, `Visitor`, `MobileApp`, `ExternalHRSystem`), and structured use case scenarios.
- **[02-domain-class-model](./02-domain-class-model)** — Conceptual domain entities (`User`, `Vehicle`, `ParkingZone`, `Slot`, `Reservation`, `Infraction`, `Invoice`, `Payment`, `Receipt`), multiplicities, and domain business rules.
- **[03-state-machine-lifecycle](./03-state-machine-lifecycle)** — Behavioral state machine specifications modeling entity lifecycles (`Invoice` settlement states: `Emitida`, `Parcialmente Paga`, `Totalmente Paga`; `Reservation` states: `Criada`, `Ativa`, `Expirada`, `Cancelada`).
- **[04-activity-workflows](./04-activity-workflows)** — End-to-end operational workflows for real-time slot reservation, RFID/LPR access control, automated no-show cancellation, and invoice debt reconciliation.
