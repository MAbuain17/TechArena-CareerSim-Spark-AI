# Decision approach and development findings

The objective is sustained career development across 48 months. Continued employment preserves future earning and advancement opportunities, while excessive defensive spending can itself weaken performance. The policy therefore ties corrective action to current evidence and resumes development as relevant conditions improve.

## Findings from v5.0

Two complete development traces exposed different failures in the same decision procedure. Both loaded the intended v5.0 Skills and ended through game elimination rather than a runtime error.

| Run | Months | Quantitative score | Ending |
| --- | ---: | ---: | --- |
| 20261030T130105Z | 18 | 19.85 | Second trust crisis |
| 20261030T133256Z | 8 | 23.18 | Prolonged financial distress |

In the first run, the agent recognised persistent organisational warnings but spent available Energy on other objectives. At one checkpoint it first selected mitigation in its reasoning, then dismissed the warnings without new evidence of improvement. Some repeated actions also produced no observed intended benefit. Mitigation occurred twice, at months 3 and 12; the agent's final summary incorrectly counted only one attempt.

In the second run, the displayed balance remained depleted and feedback described debt pressure. The agent noticed the warning but continued a recurring social commitment for a possible project opportunity. It treated the absence of a visible balance change as evidence against a financial cost. The trace does not reveal the exact contribution of each choice, but it shows that financial recovery did not remain a decision priority.

## Changes in v5.1

The revision makes active concerns persist across unrelated events. Overriding a concern requires relevant observed improvement or a more urgent competing threat. Speculative development benefits do not satisfy that requirement.

Financial recovery becomes an explicit objective when depleted balances or debt feedback persist. The agent compares the cumulative burden of commitments and avoids assuming that an unchanged displayed balance proves affordability. When no remedy is offered, it chooses the most sustainable available response and retains the concern.

Quarterly planning reserves the cost of relevant urgent remedies before optional allocation. It still allows growth when evidence improves and compares competing threats rather than treating organisational risk as the only failure direction. Outcome checks distinguish attempts from results and require reconsideration before repeating an action whose intended benefit was absent.

## Generality and evaluation

The Skills encode decision procedures, not event answers, private thresholds or a fixed monthly schedule. They use the live menu, public rules and feedback from the current session. The same procedure applies when event wording, order or available remedies change.

Version 5.1 has not yet been measured in a complete designated-model run. Offline review can identify contradictory instructions and poor responses to recorded decisions; it cannot establish a score improvement or reconstruct outcomes for actions that were not taken. Further evaluation should retain every run and assess survival, quantitative outcome and token use together. A best run alone is insufficient evidence of reliability.
