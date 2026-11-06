# Adaptive career policy: preliminary Skills design

Version 0.1, 26 October 2026. This is a proposed solution for the UK TechArena Career Survival Agent challenge. The Skills have been drafted and reviewed against the released public documentation. No live performance result is claimed at this stage.

## Task and design intent

The agent must manage a 48-month career under incomplete information. Story choices create immediate effects and possible later obligations. Quarterly choices allocate scarce resources, and periodic reviews assess sustained progress. A strong ending depends on several career dimensions; simply avoiding an early exit is not enough.

Our approach is to make a small number of clear decision procedures available to one agent. It should respond to observed vulnerability, develop the career when conditions allow, and revise its plan after feedback. It should not require an exact model of hidden game mechanics.

The runtime is JiuwenSwarm 0.2.4b3, with `mode` set to `agent`. Both Skills below are instructions followed by the same agent. There are no teammate agents, external model calls, executable scripts, or supporting reference files in this preliminary design.

## High-level design

The official runner hosts the agent, installs the submitted Skills, and supplies the simulation tools. We keep that execution path intact. The participant contribution is a concise manifest instruction and two Skills.

| Component | Responsibility | Information used | Result |
|---|---|---|---|
| Manifest instruction | Establish which Skill applies and preserve the normal game loop | Installed Skill names and official runner instructions | Clear entry point for the single agent |
| `career-controller` | Own the session, assess stories, handle reviews, reconcile uncertainty, and recognise the ending | Current observation, public handbook, current-run feedback and official logs | One legal next action with a concise reason |
| `quarterly-planning` | Compare remaining Energy allocations and the main action | Current menu and budget, visible vulnerabilities, unresolved concerns, review context | A provisional bundle and its next action |
| Working context | Retain only decision-relevant state and unresolved concerns | Observations and attributed feedback from this run | A small, revisable summary |
| Official MCP interface | Read state and apply decisions | Session ID and valid tool arguments | Authoritative public results |

The controller calls `observe`, identifies the phase, applies the relevant decision procedure, and calls `take_action` once. It then checks the returned feedback and observes before the next decision. A quarterly plan is reconsidered after every action. No component predicts an unseen branch and treats it as a real game state.

## Skill responsibilities and combination

### Career controller

This Skill applies throughout the run. It preserves the existing session, uses the current option mapping, and responds to missing context through the official observation and log tools. It also interprets story choices jointly: workload, realised benefits, learning, relationships, dignity, wealth, and future obligations may interact.

Its priorities depend on the state. A credible immediate danger deserves urgent attention. Persistent adverse trends and unresolved warnings should affect the next decision. When those concerns are absent or manageable, the agent should pursue sustainable career progress. This avoids both reckless growth and a policy that spends every opportunity on recovery.

The controller alone applies the chosen action. It records why the decision made sense from the evidence then available. Expected effects are labelled as expectations and are checked against later feedback.

### Quarterly planning

This Skill applies only when the observed phase offers quarterly Energy or a main action. It compares a small set of feasible allocations using the remaining budget and published action descriptions. It considers the main action while allocating Energy, but never relies on a later recovery to justify an unsafe intermediate step.

The planner returns a next step to the same agent's normal decision loop. It does not execute several choices at once. The current menu controls which actions and repetitions are legal.

The separation gives the controller a stable, compact role while keeping the resource-allocation procedure explicit. Adding more Skills would need a distinct responsibility and evidence that the extra instructions help. The preliminary design does not assume that more Skills improve performance.

## Information and uncertainty

| Information class | Treatment |
|---|---|
| Published rule or exposed tool schema | Use directly within its stated scope |
| Current state and available choices | Use as the authoritative decision point |
| Feedback and official logs from this run | Use to understand outcomes, warnings, trends, and unresolved commitments |
| Interpretation of story wording | Use cautiously; distinguish likely directions from known effects |
| Hidden promotion, failure, risk, or scoring mechanism | Keep unknown; do not encode an unpublished threshold or formula |
| Prior event identity or answer | Do not store or use a fixed answer mapping |

The working summary holds the current session, phase, objective, important trends, unresolved warnings or obligations, review feedback, and last attempted action. It lives in the agent context. The design does not require writing a custom state file or reading the simulation database. If context is compressed, the agent reconstructs what it can from `observe` and recent official logs. Recent logs may be incomplete, so the agent must not invent a lost commitment or assume that an absent warning proves a risk was cleared.

An action can coincide with salary, a bonus, settlement, or another change. The agent does not automatically attribute the entire difference between two observations to its choice. A single disappointing action also does not establish a hidden cap.

## Long-term decisions

The agent uses the current phase and remaining opportunities, rather than a memorised sequence of events. Early progress may provide benefits over more of the career, but promotion is uncertain and depends on sustained results. Feedback after a review can change which weakness deserves attention next.

Towards the end, the agent weighs investments against the opportunities left to benefit from them. A final review or the ending dimensions may still reward development. The policy therefore does not impose a fixed cutoff after which all growth actions are rejected.

Workplace advice is limited to interpreting an option's actual commitments and trade-offs. It is not used as a universal answer rule. General lessons from other agent systems, such as concise state, clear responsibilities, and feedback-driven revision, inform the structure without adding another runtime.

## Reliability and principal risks

| Risk | Response in the draft | What development must establish |
|---|---|---|
| Safety language suppresses useful growth | Recovery depends on observed vulnerability; healthy states favour progress | Completion and outcome distributions across repeated runs |
| Story wording encourages overconfident forecasts | Assess the whole option and retain uncertainty; no invented effect sizes | Whether notes and decisions stay tied to visible evidence |
| Budget reasoning ignores an intermediate hazard | Compare feasible bundles, execute one step, observe again | Correct Energy use and appropriate recovery ordering |
| Lost context causes a new session or stale decision | Preserve session ID; reconstruct from observation and logs | Behaviour during actual runner continuation |
| Unclear tool response causes a duplicate action | Reconcile state and logs before another mutation | Whether observed failures are handled without blind retries |
| Too much context wastes credit or obscures instructions | Short manifest, two scoped Skills, brief notes, logs on demand | Actual token use, cost, Skill loading, and decision quality |
| A development pattern is mistaken for a general law | No event lookup or unpublished threshold; current evidence stays qualified | Decisions remain applicable when context and choices vary |
| Documents claim a system the Skills do not implement | Map each design responsibility to an actual Skill section | Final consistency review after every material policy revision |

## Development and evaluation plan

First establish an end-to-end baseline with the official pinned environment and the designated model. Record complete and failed attempts, actual cost, survival length, ending score, and the generated transcript and event artifacts. Local results are development evidence, not official competition scores.

Then change one policy feature at a time. The first comparisons should test whether quarterly bundle planning improves on a simple one-step policy, whether the warning/trend summary prevents repeated mistakes, and whether a shorter wording preserves useful decisions. All variants retain the same official interface and single-agent mode.

The documented `new_game()` interface does not expose a seed argument. We therefore plan independent repeated runs and will not claim paired seeds or identical scenarios. Small samples will be reported as small samples. Compare mean career outcome, completion, lower outcomes, token usage, and concrete execution defects; do not select a version from its best run alone.

Use the initial run to estimate cost before allocating the remaining API credit. Stop spending on a variant that repeatedly creates the same clear execution defect. Keep a budget reserve for confirming the selected version and resolving setup problems. Freeze the candidate during its confirmation runs rather than changing it after each result.

Review only public rules and outputs produced by our own runs. Preserve those original outputs. Record the policy version, the observed failure, the change, and the later evidence in a separate development record. This will support an honest decision report and presentation based on actual iteration.

## Preliminary and final readiness

The preliminary package provides the manifest, this design, and two substantive Skills. It requests participation verification and makes no claim of a winning or benchmarked policy.

After API access, the final submission will add the required README, decision report, and English presentation, alongside tested revisions of these Skills. The presentation will address the organiser's five questions in order and use a real earlier-log-to-later-change example. No invented experiment or empty video will be used to complete the package.

Before submission, validate the correct archive structure, genuine team name, Skill front matter, English deliverables, exact platform version, absence of secrets, and consistency between the submitted Skills and the documents. Runtime correctness and quality require live testing beyond a structural check.

## Sources

Design basis checked on 26 October 2026:

- [Competition rules and fair play](https://techarena-career-sim.readthedocs.io/en/latest/competition-rules.html)
- [Public handbook](https://techarena-career-sim.readthedocs.io/en/latest/handbook.html)
- [Public rules](https://techarena-career-sim.readthedocs.io/en/latest/rules.html)
- [Failure and endings](https://techarena-career-sim.readthedocs.io/en/latest/failure-and-ending.html)
- [Official MCP interface](https://techarena-career-sim.readthedocs.io/en/latest/mcp.html)
- [Submission requirements](https://techarena-career-sim.readthedocs.io/en/latest/submission.html)
- [API key conditions](https://techarena-career-sim.readthedocs.io/en/latest/api-key.html)

The public participation runner was reviewed at commit `00b084a88732d81e595db88b26dde90d44e72d87` in [RAI-Internal/techarena-career-sim](https://github.com/RAI-Internal/techarena-career-sim). This review did not inspect the simulation engine or dataset internals.
