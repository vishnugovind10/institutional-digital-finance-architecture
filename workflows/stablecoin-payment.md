# Stablecoin payment

Payment intent and beneficiary → authority and policy → economic controls (FX, fees, liquidity, compliance evidence, timing) → eligible route selection → execution event → settlement evidence → treasury consequence and resulting balances → reconciliation across payment, custody, and accounting records → assurance.

A route evaluation is not a payment. A simulated execution is not a settled transfer. PayFlow Control Plane evaluates synthetic illustrative routes and does not process real payments. The architecture expects explicit failure and unknown states for expired quotes, partial processing, delayed settlement, liquidity shortfall, or reconciliation breaks.
