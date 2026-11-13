# Domain & Class Model

## Core Domain Entities & Relationships
- **`Utilizador` (`1` .. `*` `Veiculo`):** Categorized by profile (`Dirigente`, `ProfessorEfetivo`, `Investigador`, `ColaboradorAdministrativo`, `ProfessorVisitante`) dictating zone access and reservation privileges.
- **`Parque` (`1` .. `*` `Lugar`):** Physical zones (`A` reserved, `B` partially restricted, `C` intermediate, `D` open access) containing typed slots (`Coberto`, `SemiCoberto`, `Descoberto`, `MobilidadeReduzida`, `CarregamentoEletrico`, `Visitante`).
- **`Reserva` (`*` .. `1` `Utilizador`, `*` .. `1` `Lugar`):** Time-bounded booking subject to maximum duration and automatic expiration policies.
- **`Infracao` (`*` .. `1` `Utilizador`):** Penalty record (`Aviso`, `SuspensaoTemporaria`) triggered by unauthorized slot occupation.
- **`Fatura` & `Recibo`:** Financial entities governing billing amounts, outstanding balance (`divida`), and partial/full payment receipts.
