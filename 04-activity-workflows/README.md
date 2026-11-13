# Activity Workflows (`Modelo de Atividades.vpp`)

## Reservation & Automated Cancellation Workflow
1. **Fazer Login:** User authenticates via web portal or mobile app.
2. **Escolher Parque & Data/Hora:** User selects target zone and desired schedule.
3. **Verificar Permissões de Acesso:**
   - `[Sem Permissão]` -> Display access denial error and terminate flow (`[ActivityFinal]`).
   - `[Com Permissão]` -> Proceed to availability check.
4. **Verificar Disponibilidade de Lugares:**
   - `[Indisponível]` -> Execute `Mostrar indisponibilidade` and terminate flow.
   - `[Disponível]` -> Execute `Confirmar reserva` -> `Registar reserva no sistema` -> `Enviar notificações ao utilizador`.
5. **Esperar Uso da Reserva:**
   - `[Utilizada dentro do tempo-limite]` -> Register entry and complete workflow.
   - `[Não utilizada após tempo-limite]` -> Execute `Cancelar reserva automaticamente` and release slot.
