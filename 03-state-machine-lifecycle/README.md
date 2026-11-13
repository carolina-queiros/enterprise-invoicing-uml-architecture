# State Machine Lifecycles

## 1. Invoice Settlement State Machine (`ex fatura.vpp`)

| Source State | Event / Trigger | Guard Condition | Action / Effect | Target State |
|---|---|---|---|---|
| `[Initial]` | `emitir()` | — | — | `Emitida` |
| `Emitida` | `pagar()` | `[valor < divida]` | `calcularDivida()` | `Parcialmente Paga` |
| `Emitida` | `pagar()` | `[valor = divida]` | `entry / emite recibo` | `Totalmente Paga` |
| `Parcialmente Paga` | `pagar()` | `[valor < divida]` | `calcular divida`; `entry / emite recibo` | `Parcialmente Paga` |
| `Parcialmente Paga` | `pagar()` | `[valor = divida]` | `entry / emite recibo` | `Totalmente Paga` |
| `Totalmente Paga` | — | — | — | `[Final]` |

## 2. Reservation Lifecycle State Machine
- **States:** `Criada` -> `Ativa` (upon check-in within grace period) -> `Concluida` | `Expirada` (automated timeout cancellation) | `Cancelada` (user-initiated).
