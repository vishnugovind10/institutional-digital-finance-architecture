# Execution and settlement

Execution records what a venue accepted, rejected, partially filled, or left uncertain. Settlement records whether the intended asset and cash obligations transitioned, under which finality rule and evidence. These are separate state machines connected by stable intent and event identifiers.

For DvP, model asset and cash legs, eligibility, authorization, availability, synchronization, atomicity assumptions, finality, timeout, and recovery. A partial fill or one-sided state must remain visible as an exception. Do not infer settlement from an execution acknowledgement or a single chain event without the required context.

See the Institutional Settlement State Machine and Institutional Digital Collateral Stack. OMST provides an experimental vocabulary for describing monetary state and transition compatibility.
