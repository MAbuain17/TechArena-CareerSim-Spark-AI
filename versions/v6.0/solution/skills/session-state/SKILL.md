---
name: session-state
description: Start or recover a CareerSim session and interpret every new observation. Use before deciding; observe again after each action, including multiple decisions within the same month.
---

# Session and evidence

Maximise the final career outcome across 48 months. One agent owns the session. Read the handbook once, start new_game once and print SESSION_ID=<id>. Preserve an existing session. Use only the official five game tools: new_game, observe, take_action, check_latest_logs and show_employee_handbook. Use the designated model in JiuwenSwarm 0.2.4b3 agent mode. Do not inspect engine packages, use other agents, external memory, hidden formulas or route overrides.

Read the live event, all choices, costs, statistics, feedback and phase. A month can contain several events and follow-ups. Identify phases from the returned interface, not month alone. Reviews may already have settled before the next allocation. Never plan to improve a review already returned.

Maintain a working record: current objective; latest review; resource trends; unresolved warnings; commitments; last action and verified result. Distinguish explicit facts, plausible consequences and unknowns. Hidden risk is not a visible measured balance: preserve actual feedback instead of inventing Low/Medium/High scores or counters. Do not compare the smallest raw number across unlike scales.

After every take_action, observe before acting again. Verify actual changes against the previous state, accounting for salary, settlement and intervening events. Advertised gains are expectations, not achieved results. After a material unexpected outcome, use a small recent log window if it can clarify the decision. Unchanged rounded/displayed values do not establish a cap, zero cost or failed mitigation.

Write useful notes: objective; decisive trade-off; unresolved concern and latest response; next check. Carry a fuller checkpoint at quarterly boundaries, reviews and material warnings. Do not copy the complete transcript. After context loss, observe and retrieve recent notes, expanding only if necessary. Reconcile uncertain execution before retrying. Never restart to escape a bad trajectory. Stop only at the official ending, return its full ending_score and DONE.
