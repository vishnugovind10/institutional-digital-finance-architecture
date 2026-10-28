# Control-plane matrix

| Control | Question | Input | Decision / state | State affected | Evidence |
|---|---|---|---|---|---|
| Authority | Who may act? | Identity, mandate, delegation, time | Allow / deny / expire | Authority state | Authorization record and policy version |
| Economic control | Should the action proceed? | Price, risk, liquidity, alternatives | Approve / deny / conditional | Decision state | Inputs, exclusions, reason record |
| Execution | What happened at the venue? | Approved intent, venue events | Accepted / partial / failed / unknown | Execution state | Venue event and correlation ID |
| Settlement | Did intended obligations transition? | Asset/cash events, finality rule | Settled / pending / failed / divergent | Settlement state | Scoped settlement evidence |
| Financial state | What obligations and positions exist? | Settlement and source events | Position/balance/obligation update | Financial state | Lineage and effective/observed time |
| Liquidity | Can obligations be funded when due? | Cash, location, amount, time | Sufficient / insufficient / unknown | Liquidity state | Time-bucket calculation and assumptions |
| Exposure | Is combined risk within limits? | Positions, commitments, agent actions | Within / breach / incomplete | Exposure state | Aggregate set and exclusions |
| Reconciliation | Do internal and external records agree? | Independent records and rules | Match / break / incomplete | Accounting state | Match keys, tolerances, break record |
| Assurance | Can a bounded claim be supported? | Evidence, scope, freshness | Supported / unsupported / abstain | Assurance state | Evidence package and limitations |
