# Institutional delivery-versus-payment

Specify trade intent, parties, asset and cash legs, eligibility, authority, and available balances. A decision checks policy and liquidity before execution. Coordination must define whether legs are atomic, what evidence establishes finality, and how timeouts or one-sided completion are handled. Settlement state then drives positions and obligations; liquidity/exposure is recomputed; independent records are reconciled; evidence supports closure or escalation.

OMST is an experimental/open reference specification for monetary state/transition compatibility, not an adopted standard. Institutional Settlement State Machine and Institutional Digital Collateral Stack provide separate executable references. No interoperability between these repositories is implied.
