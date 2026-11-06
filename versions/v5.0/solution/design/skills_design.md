# Skill architecture

One agent owns the session and makes every decision. The two Skills separate continuous control from quarterly allocation. They share one objective and one working context.

## Career controller

The controller reads the current observation, interprets feedback and chooses a feasible response. It considers the consequences of acting and delaying, including costs that are not expressed as Energy or cash. For a consequential choice, it compares the preferred response with a credible alternative and preserves the safeguards stated in each option.

The controller executes one action, waits for its result and observes before making another decision. This keeps execution aligned with the live menu. It distinguishes an accepted action from a confirmed benefit, and checks whether settlement or intervening events could explain a change.

Its working context contains the current objective, latest review, material open concerns, commitments and relevant confirmed outcomes. Notes preserve the parts needed after context loss. They exclude repeated history and gains that have not occurred. Recovery uses the existing session, the current observation and a small relevant log window.

## Quarterly planning

The planner compares the remaining Energy allocation and the separate main action. It identifies the current constraint from warnings, trajectory and review feedback. It considers competing needs together so optional spending does not consume resources needed for a more urgent response.

Its plan is provisional. Only the next action is executed; the remaining allocation is reconsidered after observation. Exact benefit comparisons use exposed magnitudes. Directional effects alone do not establish that one bundle dominates another.

The planner balances recovery with continued development. It avoids buying increases in Health or Dignity that already sit at the published limit, while allowing recovery that protects against credible upcoming costs. It compares each main action with a relevant alternative instead of defaulting to a familiar project.

## Shared priorities

The agent protects against credible early failure, including persistent weak performance, isolation and financial distress. It then pursues sustainable progress across the ending dimensions. A warning changes the assessment, but its remedy depends on the concern and the offered actions. Good performance does not cancel a separate organisational warning; an old warning does not justify permanent defensive spending after relevant evidence improves.

Reviews and material new evidence trigger strategic reassessment. Routine turns apply the current objective without repeatedly rebuilding the whole plan. The remaining horizon limits which delayed benefits are useful, using actual returned phases rather than fixed development-event timing.

## Runtime integration

The manifest carries the compact session and decision procedure. The controller is loaded at the start; the planner is loaded when quarterly allocation first appears. Instructions are reused while available and recovered when necessary.

The official tools provide observation, execution, the handbook and recent logs. The policy therefore needs no additional executable component or reference service. This keeps the runtime focused on decisions from the current run and makes the procedure straightforward to inspect.
