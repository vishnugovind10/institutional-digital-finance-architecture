# Existing work: architecture map

Public GitHub repository pages, README files, top-level artifacts, descriptions, and implementation footprints were inspected on 2026-10-28. Scores use institutional relevance (20%), architecture depth (20%), implementation (15%), market relevance (15%), uniqueness (10%), discoverability (10%), and coherence (10%), on a 1–5 scale normalized to 100. They assess fit for this architecture, not overall quality.

## Selected references, ranked

| Rank | Repository | Layer | Score | Reason / credibility signal | Search terms |
|---:|---|---|---:|---|---|
| 1 | [institutional-digital-collateral-stack](https://github.com/vishnugovind10/institutional-digital-collateral-stack) | Collateral, settlement, liquidity, reconciliation | 98 | Executable Python reference with specification, tests, scenarios and docs; synthetic deterministic data. | institutional settlement, digital collateral, DvP, liquidity |
| 2 | [open-monetary-state-transition-standard](https://github.com/vishnugovind10/open-monetary-state-transition-standard) | Monetary state and interoperability | 97 | Specification, schemas, conformance, adapters, scenarios and tests; experimental/open reference specification, not adopted industry standard. | digital money, monetary state, settlement interoperability |
| 3 | [institutional-settlement-state-machine](https://github.com/vishnugovind10/institutional-settlement-state-machine) | Settlement coordination | 95 | Chain-agnostic Python model, schemas, conformance material, scenarios and tests. | DLT settlement, state machine, finality |
| 5 | [payflow-control-plane](https://github.com/vishnugovind10/payflow-control-plane) | Payment decisioning | 91 | Tested Python control plane evaluates synthetic routes across authority, compliance evidence, FX, liquidity, and treasury impact; does not process real payments. | stablecoin infrastructure, payment routing, treasury |
| 4 | [Canton-Control-Plane](https://github.com/vishnugovind10/Canton-Control-Plane) | Distributed financial state / synchronization | 92 | TypeScript engine with architecture docs, schema, topology, and examples for Canton synchronization state. | Canton Network, distributed ledger, synchronization |
| 7 | [institutional-digital-asset-assurance](https://github.com/vishnugovind10/institutional-digital-asset-assurance) | Assurance and evidence | 87 | Tested Python controls, dated scenarios, static console; synthetic reference implementation. | digital asset assurance, evidence, institutional controls |
| 6 | [navbridge](https://github.com/vishnugovind10/navbridge) | NAV reconciliation | 89 | Python implementation and tests classify tokenized-fund NAV divergence; does not choose which NAV is correct. | tokenized funds, NAV integrity, reconciliation |
| 8 | [agentic-financial-consequence](https://github.com/vishnugovind10/agentic-financial-consequence) | Agent consequence / assurance | 86 | Tested Python reference binds authorized intent to execution, settlement, liquidity, reconciliation, and consequence. | agentic finance, financial state, consequence assurance |
| 9 | [agent-trust-probe](https://github.com/vishnugovind10/agent-trust-probe) | Agent identity and authority | 83 | Python package, specifications, tests, and examples for bounded agents and agency relationships. | AI agents in finance, delegated authority, agent identity |
| 10 | [canton-proofpack](https://github.com/vishnugovind10/canton-proofpack) | Scoped assurance for private ledger views | 82 | Python package, tests, and docs produce party-scoped evidence and disclose trust/visibility boundaries. | Canton, privacy-preserving ledger, audit evidence |
| 11 | [temporal-liquidity-risk](https://github.com/vishnugovind10/temporal-liquidity-risk) | Liquidity timing and stress | 75 | Small simulation illustrates synchronized demand causing settlement failure despite sufficient collateral; limited scope. | liquidity risk, tokenized settlement, treasury |

Rank reflects strategic layer coverage as well as score; the score is not a strict cutoff. These repositories represent independent artifact types: reference architecture, state machine, control plane, experimental specification, observability, simulation, reconciliation, and assurance. Their relationship here is **conceptual**; no shared runtime, data plane, or tested integration is claimed.

## Candidate score record

| Candidate | Inst. 20 | Arch. 20 | Impl. 15 | Market 15 | Unique 10 | Search 10 | Coherence 10 | Total /100 | Decision |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| institutional-digital-collateral-stack | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 96 | Select |
| open-monetary-state-transition-standard | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 94 | Select |
| institutional-settlement-state-machine | 5 | 5 | 5 | 5 | 4 | 4 | 5 | 95 | Select |
| payflow-control-plane | 5 | 4 | 4 | 5 | 4 | 5 | 5 | 90 | Select |
| Canton-Control-Plane | 5 | 5 | 3 | 5 | 4 | 5 | 5 | 90 | Select |
| institutional-digital-asset-assurance | 5 | 4 | 4 | 5 | 3 | 4 | 5 | 86 | Select |
| navbridge | 5 | 4 | 4 | 5 | 4 | 4 | 5 | 88 | Select |
| agentic-financial-consequence | 4 | 4 | 4 | 4 | 5 | 5 | 5 | 86 | Select |
| agent-trust-probe | 4 | 4 | 4 | 3 | 5 | 5 | 5 | 82 | Select |
| canton-proofpack | 4 | 4 | 4 | 4 | 4 | 4 | 5 | 82 | Select |
| temporal-liquidity-risk | 4 | 3 | 3 | 4 | 4 | 4 | 5 | 75 | Select, limited scope |
| control-probe | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 80 | Exclude: overlaps selected assurance/control examples |
| canton-sync-debt-observatory | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 60 | Exclude: inspected as a Daml observability example; less direct fit than the selected Canton references |
| haircut | 4 | 3 | 4 | 4 | 3 | 4 | 4 | 74 | Exclude: narrower than selected collateral and liquidity examples |
| tokenize-stack | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 78 | Exclude: overlaps collateral and settlement coverage |
| warrant | 3 | 4 | 4 | 3 | 4 | 4 | 4 | 73 | Exclude: adjacent agent constraint mechanism; selected references cover authority and consequence |
| correlation-governor | 4 | 3 | 4 | 4 | 4 | 4 | 4 | 76 | Exclude: useful aggregate-agent stress proof but narrower than selected lifecycle examples |
| canton-observer | 3 | 3 | 4 | 3 | 4 | 3 | 3 | 65 | Exclude: bounded-view auditor overlaps scoped Canton evidence |
| liquid-proofpack | 3 | 4 | 4 | 3 | 4 | 3 | 3 | 69 | Exclude: relevant but ledger-specific beside Canton ProofPack |
| agentic-economy-observatory | — | — | — | — | — | — | — | — | Exclude: public repo had no README/description sufficient to validate relevance or implementation |
| agentic-finops-ledger | — | — | — | — | — | — | — | — | Exclude: private; cannot be represented as a public reference |

## Maturity and accuracy

The selected links were public when checked. Artifact descriptions above are based on repository contents; they do not establish production deployment, customer use, institutional adoption, or integration with this architecture. Review each source repository's limitations and current state before relying on it.
