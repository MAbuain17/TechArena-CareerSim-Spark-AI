# Decision strategy and evaluation

**Team:** Spärk AI  
**Participant:** Mohamed Abuain  
**Candidate:** career-survival-uk-v4.3-verified-decisions

V4.3 has not yet been run. Results below belong to earlier policies. The v4.2 event stream, transcript and score report were inspected for this revision; older run summaries are retained from the supplied development report.

## Strategy

The agent aims to complete 48 months while building sustainable career value. It first addresses credible immediate threats, then unresolved adverse feedback, and otherwise invests in development. Decisions use the public handbook, current choices, exposed costs, review grades and feedback returned within the session.

The controller separates organisational risk from visible performance. A positive review or rising Output can coexist with unresolved exposure. Following an incident or persistent warnings, relevant mitigation takes priority over optional exposure-increasing growth. Once feedback improves, the agent resumes development rather than remaining permanently defensive.

Quarterly planning compares the remaining Energy allocation with the main-action opportunity. It commits one step at a time and checks the result before continuing. Promotion planning considers sustained delivery, capability and relationships; exact promotion thresholds are not assumed.

## Development results

The following local runs were reviewed using their structured event streams and score reports. Scores are individual development outcomes, not official three-run evaluation scores. Run identifiers are UTC timestamps.

| Policy | Run ID | Months | Outcome | Level | Score / 100 | Total tokens | Tokens / month |
|---|---|---:|---|---|---:|---:|---:|
| Baseline | `20261026T233241Z` | 26 | eliminated | L3 | 27.57 | 17,791,187 | 684,276 |
| Survival-first v2 | `20261027T002002Z` | 24 | eliminated | L1 | 29.01 | 17,074,116 | 711,422 |
| Adaptive policy | `20261027T184953Z` | 48 | completed | L4 | 52.33 | 61,671,146 | 1,284,816 |
| v4.1 / iteration 3 | `20261027T210643Z` | 16 | eliminated | L3 | 26.38 | 10,934,243 | 683,390 |
| v4.1 / iteration 3.1 | `20261027T212840Z` | 42 | eliminated | L5 | 58.58 | 43,806,432 | 1,043,010 |
| Baseline v4.2 | `20261027T221931Z` | 48 | completed | L5 | 67.28 | 56,855,219 | 1,184,484 |

Each run is recorded under `.career_sim_runner/career_emu/outputs/<team-or-local-label>/<run-id>/`, with `events-<run-id>.jsonl`, `transcript-<run-id>.log` and `score_report.json`. Run references below identify the evidence without placing replay data in the agent's Skills.

## Findings and design changes

### Balancing development and survival

The baseline ended after 26 months. The survival-first revision ended after 24 months at L1, showing that a defensive policy still needs sustained development. The adaptive policy completed 48 months at L4 with 52.33 points. These runs established the need to preserve growth while improving verification and responses to warnings.

### Turning warnings into action

Iteration 3.1 (`20261027T212840Z`) reached L5 but ended in a second trust crisis at month 42. At turn 96, month 24, the observation reported a major organisational incident. At turn 98, the agent selected high-intensity work to rebuild Output. It selected high-intensity work again at turn 136, month 33, and turn 161, month 39, despite recurring risk warnings. Across the run it chose seven high-intensity actions and twelve key projects, with no legacy-risk mitigation.

V4.2 makes this distinction explicit: restoring delivery does not repair the cause of an incident. The agent retains the unresolved concern and prioritises a relevant response before optional growth that adds exposure. Quarterly decisions compare the preferred growth action with a lower-exposure or mitigation alternative. Short action notes must identify the current evidence and trade-off.

### Latest completed run

Run `20261027T221931Z` completed all 48 months with 67.28 points. The trajectory shows risk mitigation at turns 36 (month 9), 72 (month 18), 85 (month 21), 96 (month 24), 108 (month 27), 157 (month 39) and 194 (month 48). The notes at turns 72 and 157 explicitly connect persistent HR warnings to mitigation priority.

Development continued: the agent selected fifteen key projects and five high-intensity actions. Promotions occurred at months 12, 18, 24 and 48, ending at L5. The terminal observation is turn 197; the score report records 48 months survived.

| Ending dimension | Result | Score contribution |
|---|---:|---:|
| Career level | L5 | 15.00 / 30 |
| Wealth | 27.8 | 6.95 / 20 |
| Health and dignity | 10 and 10 | 15.00 / 15 |
| Professional skill | 112 | 14.00 / 15 |
| Risk control | 100/100 normalised | 10.00 / 10 |
| Relationships | Network 38 | 6.33 / 10 |
| **Total** | | **67.28 / 100** |

Compared with iteration 3.1, the latest run survived six additional months and scored 8.70 points more. Risk-control contribution increased from zero to ten points. The two runs followed different trajectories; further repeated runs are needed to assess reliability.

## Efficiency and remaining opportunities

The latest run used 56,855,219 tokens, or approximately 1,184,484 per surviving month. The earlier completed adaptive run used approximately 1,284,816 tokens per month. These measurements track the full recorded interaction, including repeated input context; they do not isolate the effect of shorter notes.

The policy reuses loaded instructions, limits log retrieval to specific uncertainties and executes one action per decision. Further evaluation should measure repeated observations, unnecessary context and delays between selecting and executing an action. Career level, wealth and relationships retain the largest score headroom in the latest result. Improving them must preserve the observed survival and risk-control behaviour.

## Generalisation and evaluation

The Skills use current menus, costs, observations and review feedback rather than event-specific answers or learned hidden thresholds. They reassess after missing gains, changed circumstances and new warnings. This supports adaptation to different event sequences and resource conditions.

The next evaluation should repeat the submitted policy across complete runs and compare survival, quantitative score, warning-to-action behaviour, advancement, action validity and tokens per month. One completed run establishes successful execution, while repeated runs are needed to measure consistency. The local structure, manifest and Skill-front-matter checks complement this behavioural evaluation.

## V4.3 changes

The v4.2 run loaded both Skill texts contained in the supplied submission. It completed 197 action calls successfully. The handbook was read once and each Skill once. No recent-log calls were recorded.

### Outcome verification

High-intensity work at months 6, 33 and 42 produced no observed Output increase in the next observation while Health and Dignity fell. V4.3 requires a comparison with an alternative before repeating an absent benefit. A repeat needs a current reason, recorded briefly with the preceding verified result. These observations do not establish a hidden cap.

At month 15, two Energy actions were executed without an intervening observation. V4.3 explicitly requires the returned observation before every subsequent choice, including steps within a provisional allocation.

### Allocation and risk response

The live menu permitted repeated inexpensive actions. V4.3 compares bundles by useful benefits and full costs, including wellbeing and subsequent mitigation, rather than treating high-intensity work as the default Output investment.

At month 36, warnings persisted, but the allocation used recovery, networking and report preparation. After recovery, two Energy remained for a relevant risk response. V4.3 requires unresolved concerns to be reconsidered at that point; avoiding additional exposure alone does not resolve them.

### Final-phase choices

The final main action was a key project justified partly by Output as an ending benefit, despite the returned final review. V4.3 requires comparison with directly useful ending benefits when no further review is supported. This changes the decision procedure without prescribing a fixed final action.

### Faithful option comparison

The emergency-hotfix decision at month 32 understated the safeguards offered by an alternative. V4.3 requires the agent to compare the actual safeguards and costs, distinguish explicit facts from uncertain consequences, and include the harm of delay.

### Efficiency

V4.2 used 56,855,219 tokens, approximately 1,184,484 per month, with a reported model cost of $1.678791. Input accounted for approximately 99.79% of recorded tokens. Repeated handbook loading was not the cause. V4.3 reduces routine narration and keeps working context focused on the next decision. Token savings remain unmeasured.

## Evaluation of the candidate

Structural checks and offline decision cases assess the package and instruction coverage. They do not establish performance with the competition model. The next authorised local run should retain all three official output files and compare survival, quantitative score, score components and tokens per surviving month with v4.2.

Inspect whether missing gains change subsequent choices, risk responses survive intervening recovery actions, every action is followed by observation, and final-phase comparisons use supported benefits. Keep the v4.2 baseline unchanged. Repeated complete runs are needed to assess reliability; one changed trajectory cannot isolate the effect of an individual instruction.
