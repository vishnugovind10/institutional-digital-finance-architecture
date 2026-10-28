# Reference architecture

## Lifecycle and ownership

The control path is **mandate → authority → economic decision → authorized execution → settlement → financial state → liquidity/exposure → reconciliation → assurance → institutional decision**. The lifecycle is a logical architecture; real systems may be asynchronous, distributed, and partially observable.

| Boundary | Owns | Must not imply |
|---|---|---|
| Mandate | Objectives, limits, accountable decision owners | A mandate is not an executable authorization |
| Authority | Identity, delegation, scope, validity, revocation | Permission does not establish economic suitability |
| Decision | Policy, price, risk, liquidity and alternatives at a defined time | A decision is not evidence of execution |
| Execution | Venue request, acceptance, fills, failures | Acknowledgement is not settlement |
| Settlement | Asset/cash obligations and state transition/finality | A transaction hash alone may not establish intended finality |
| Financial state | Positions, balances, obligations, receivables/payables | A local ledger view may be incomplete |
| Liquidity/exposure | Amount, currency, timing, concentration, aggregation | Collateral value does not guarantee time-specific funding |
| Reconciliation | Comparison across independently owned records | A match does not prove all inputs were complete |
| Assurance | Evidence lineage, freshness, scope, exceptions | Evidence cannot exceed the observer's visibility |

## Design principles

1. Keep authority, economic approval, execution, settlement, and assurance as distinct states and records.
2. Bind decisions to the intent, constraints, time, and evidence actually evaluated.
3. Model obligations with amount, currency, owner, due time, and state; assess liquidity over time, not only totals.
4. Make partial completion, uncertainty, stale evidence, and divergence explicit outcomes.
5. Track observer scope: absence from a bounded view is not proof of global absence.
6. Aggregate exposure across actions and actors before concluding that each action is safe.
7. Preserve identifiers and lineage across system boundaries for reconciliation.

## Systems around the control path

Identity and policy inform authority; risk, treasury, and custody inform decisions; execution venues, payment rails, tokenized assets, and DLT networks produce events; accounting and external records feed reconciliation; operational observers produce evidence. Interfaces and ownership vary by institution. This repository specifies no vendor API or production connector.
