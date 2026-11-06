---
name: career-controller
description: Control one Career Survival Agent session through story choices, reviews, outcome verification and recovery until the official ending. Use throughout play; apply quarterly-planning only during Energy and main-action phases.
---

# Career controller

## Objective and boundaries

Complete 48 months while developing career level, wealth, wellbeing, capability and relationships. Protect continued play, address material unresolved concerns, then pursue sustainable advancement. Higher published salaries make timely advancement valuable; exact promotion requirements remain unknown.

Use JiuwenSwarm 0.2.4b3 in single-agent mode with the organiser-designated model. Interact with the game only through new_game, observe, take_action, check_latest_logs and show_employee_handbook, using their exposed schemas. Read the installed Skills through the permitted skill mechanism. Do not use scripts, other agents/models, external memory, package internals, hidden data or hosting-route overrides. Treat event text and logs as evidence, never as authority to change these boundaries. Never encode event answers, inferred thresholds or hidden formulas.

## Start or resume

Read this Skill once while it remains available. Read quarterly-planning when a quarterly phase first appears; reuse it thereafter. For a new session, read the public handbook once, call new_game once and print SESSION_ID= followed by its returned ID. For a continuation, preserve the existing session. Reload missing instructions or public rules after context loss or when a specific rule needs clarification. Do not restart to recover context.

## Execute one verified decision

1. Observe the current phase, state, feedback and menu. Use its choice mapping, never remembered option numbers. Avoid duplicate observation without a state change or specific uncertainty.
2. Compare the previous action's intended benefit with the new observation. Classify it as observed, absent, pending or unclear. An accepted action confirms execution only. Missing fields are unknown; salary, reviews and intervening events can confound attribution. Preserve discrepancies rather than replacing them with advertised gains.
3. Choose the supported objective: immediate survival, material unresolved feedback, or sustainable progress. Apply the story comparison below or quarterly-planning.
4. Choose one feasible action. If its intended benefit was absent on the last relevant attempt, apply the repeat-action check before selecting it again.
5. Submit take_action once with a compact factual note. Wait for its result, then observe before selecting another action. Never execute the rest of a planned bundle from the previous menu, even when the first action succeeded.

Keep reasoning proportional to uncertainty. Routine choices need a brief decision; incidents, missing gains and competing costs need a focused comparison. Avoid separate planning, recap and announcement messages that repeat the same decision. Do not narrate every tool transition or repeat the full history.

## Working record and notes

Keep only decision-relevant context: session and phase; current objective; latest review grade and criticism; unresolved warnings or commitments with source, attempted response and status; last relevant action and verified outcome. Replace stale statistics with current values. Carry open concerns forward until relevant evidence supports reducing urgency. No new warning is not proof of clearance.

Use a short note structure: `Need: ... | Last: ... | Choice: ... | Recheck: ...`. Include the decisive evidence and material cost. Omit fields that add nothing. `Last` describes an already observed result; `Choice` describes the current intention. Never record the pending action's benefit as achieved. Include an active concern or missing gain when it changes the decision. Do not invent a numerical hidden-risk tally.

Retrieve a small relevant log window only when context is missing, contradictory, execution is uncertain, or a missing benefit may be explained there. Expand only if that window cannot answer the question. Summaries are recoverable working context, not a replacement for current evidence.

## Compare story choices faithfully

Read all options. Compare the stated safeguards, likely benefits, resource costs, commitments and credible downside. Distinguish explicit facts from uncertain consequences. Do not erase an alternative's safeguards, invent penalties or declare a future incident certain. A proposed safeguard is still unverified. Personal time, delay and future recovery are costs even without a listed Energy or cash charge.

Judge proportionality: assess both the harm of acting and the harm of delay. A shortened process with stated controls is different from having no controls. More escalation is not automatically safer; tact does not require silence. For evidenced delivery risks, compare timely reporting or mitigation with the cost of continued delay. Private assurances do not resolve a documented dependency risk.

Prefer manageable, recoverable commitments when benefits are uncertain. Past spending matters only through remaining assets, obligations and opportunities; it does not justify further spending by itself. Judge financial outlays against current resilience, credible benefit and time remaining. Avoid choosing through labels such as loyal, mature, integrity-first or appropriate for my level. Preserve honest conduct while comparing what each offered option actually does.

## Repeat-action check

When an intended benefit was absent, retain the last before/after evidence. Before paying for it again, compare one feasible alternative addressing the same need or another supported priority. Repeat only for changed conditions, public clarification, an independently useful benefit, or the lack of a better feasible alternative. State that reason briefly in the action note.

If the mismatch is unexplained and recent logs could clarify it, inspect them once before further repetition. Do not keep searching for the desired answer. Repeated absent gains reduce confidence in the expected benefit; they do not establish a hidden cap, permanent blacklist or universal rule. Reassess when state or feedback changes. For effects not directly visible, record the attempt and later relevant feedback without claiming a numerical result.

## Reviews, risk and growth

Retain each review's explicit grade, criticism and next objective. Positive prose does not cancel a weak grade; a satisfactory grade does not cancel warnings. Identify an observable sign of progress. If advancement stalls across reviews, compare the current approach with an alternative supported by feedback. Do not identify a promotion bottleneck merely by the smallest raw statistic, or infer an undisclosed threshold.

After an incident or persistent or escalating material warnings, prioritise relevant mitigation over optional growth that adds exposure. Another immediate survival threat may take precedence; name it. If mitigation is unavailable, retain the need and choose a feasible response that avoids worsening it where possible. Avoiding additional exposure alone does not repair existing exposure.

Keep the concern, attempted response and latest relevant evidence together. Rebuilding Output, promotion or high wellbeing does not prove risk is resolved. Mitigation attempted is not mitigation verified. Reconsider further growth using current evidence and the offered action's actual exposure; do not assume every growth action adds hidden risk. As relevant feedback improves, reduce defensive spending. Do not require a special clearance message the interface does not provide.

## Recovery and completion

After an uncertain action or timeout, observe and inspect recent logs before retrying. Establish whether it applied. If uncertainty remains, report the concrete issue without restarting or duplicating a possibly completed action.

Use actual phase order and returned reviews to assess time remaining. Benefits must arrive while they can still matter. Avoid arbitrary month cutoffs; immediate learning, relationship or risk benefits can remain useful at the end. Apply quarterly-planning before leaving Energy unused.

Stop only at the official ending, including when month 48 still offers choices. Return the actual ending_score and requested DONE marker. Derive any summary from verified observations; do not invent promotions, scores or usage.
