# Control failure taxonomy

| Failure | Location | Affected financial state | Detection | Control response | Block execution? | Remediation / escalation |
|---|---|---|---|---|---|---|
| Stale authority | Authority | Permission/delegation | Expiry/revocation check | Deny and refresh | Yes, before dispatch | Authority owner review |
| Policy failure | Governance/decision | Mandate limits | Versioned policy evaluation | Deny with reason | Yes | Policy owner review |
| Economic constraint failure | Decision | Cost, risk, liquidity | Hard-limit evaluation | Reject or request new decision | Yes | Treasury/risk approval |
| Execution failure | Venue | Requested action/obligation | Venue status/timeout | Keep failed or unknown; do not book completed state | Before downstream booking | Retry only under idempotency rules; escalate ambiguity |
| Partial execution | Venue | Partially filled positions/obligations | Fill aggregation | Record partial state and recalculate controls | Block remainder if limits/intent require | Reauthorize remainder where needed |
| Settlement failure | Settlement | Unfulfilled asset/cash leg | Settlement status/finality rule | Keep pending/failed; contain unmatched leg | Block dependent actions | Recovery and counterparty escalation |
| Settlement divergence | Settlement | Conflicting leg states | Cross-leg state comparison | Freeze closure; exception | Yes for dependent lifecycle | Reconcile and resolve one-sided state |
| Liquidity shortfall | Treasury | Due obligation | Time-bucket funding check | Reject, resize, or contingency fund | Yes where obligation cannot be met | Treasury escalation |
| Exposure breach | Risk/state | Aggregate position or counterparty exposure | Aggregate limit monitor | Stop new exposure; contain | Yes for incremental action | Risk escalation and reduction plan |
| Synchronization divergence | Distributed state | Incomplete/stale ledger view | Offset/lag and observer checks | Mark view incomplete; avoid unsafe action | Yes if control depends on completeness | Restore sync and compare scoped views |
| Reconciliation divergence | Reconciliation | Accounting/position records | Matching and break classification | Keep break open; suspend closeout | Block closeout, not necessarily all execution | Assign owner and resolve/escalate |
| Stale valuation/NAV | Valuation | Marks and derived exposure | As-of/freshness check | Mark valuation stale; rerun decision | Yes if threshold depends on it | Refresh source and review impact |
| Evidence failure | Assurance | Confidence in lifecycle claim | Integrity, scope, freshness validation | Abstain from assurance claim | Block only if evidence is a precondition | Recollect and preserve gap record |
| Agent aggregate-exposure breach | Cross-agent risk | Combined commitments/exposure | Shared exposure aggregation | Stop additional actions; contain pending commitments | Yes for new actions | Institutional risk owner review |

Blocking is policy-specific. The table identifies a safe default at the affected boundary; it does not prescribe a universal institutional rule.
