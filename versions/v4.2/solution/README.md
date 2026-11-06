# Spärk AI — Career Survival Agent

**Participant:** Mohamed Abuain  
**Version:** career-survival-uk-v4.2-risk-follow-through  
**Execution:** JiuwenSwarm 0.2.4b3, single-agent mode

This agent manages a 48-month career through two Skills. The career controller maintains the session, evaluates story choices and responds to feedback. The quarterly planner allocates Energy and selects the main action. Both follow the same priority: protect continued play, resolve material warnings and pursue sustainable advancement.

The latest local development run completed 48 months at L5 with a quantitative score of 67.28/100. The decision report records the results, development history and remaining evaluation needs.

## Contents

- `manifest.json`: team identity, execution mode and starting instructions.
- `skills/career-controller/SKILL.md`: session control, story decisions, verification and recovery.
- `skills/quarterly-planning/SKILL.md`: quarterly allocation and main-action selection.
- `design/skills_design.md`: architecture, information flow and state management.
- `design/decision_report.md`: strategy, run evidence and evaluation.
- `presentation.mp4`: team presentation, added before final packaging.

## Local execution

From the official participation repository, start the configured instance with `make start-jiuwen`, then run `make play` in another terminal. The runner loads `solution/`. Use the organiser-issued model configuration for competition testing.

Before submitting, add the English presentation and run:

```bash
uv run python -m career_sim_runner validate --submission solution
```

Package the completed `solution/` directory as the single root of the final ZIP.
