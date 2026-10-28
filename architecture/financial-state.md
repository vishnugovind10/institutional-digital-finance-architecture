# Financial state

Represent the post-action state as owned positions, balances, obligations, and contingent exposures with currency/asset, quantity, counterparty, source, effective time, observation time, and status. Preserve pending, disputed, failed, and unknown states; do not silently collapse them into settled balances.

Financial state is distributed across ledgers and institutions. Every view has a scope and freshness boundary. State transitions should retain causal references to the mandate, decision, execution, settlement, and source events that produced them. This reference architecture does not prescribe a universal ledger or claim global visibility.
