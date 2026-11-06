# Spärk AI Career Survival Agent

**Participant:** Mohamed Abuain  
**Version:** career-survival-uk-v4.3-verified-decisions  
**Execution:** JiuwenSwarm 0.2.4b3, single-agent mode

The career controller manages session continuity, story decisions, feedback and verification. The quarterly planner compares Energy allocations and main actions. Both use current official observations and retain unresolved concerns until relevant evidence supports changing priorities.

V4.3 adds explicit checks before repeating ineffective actions, compares cheaper action combinations, and strengthens risk follow-through and final-phase decisions. The preceding v4.2 run completed 48 months at L5 with 67.28 points. V4.3 is a new candidate awaiting gameplay evaluation.

## Files

- `manifest.json`: team identity and starting instructions.
- `skills/`: the two gameplay Skills.
- `design/skills_design.md`: responsibilities, information flow and decision procedure.
- `design/decision_report.md`: baseline evidence, changes and evaluation plan.

## Local evaluation

Place this directory in the official participation repository as `solution-v4.3` to keep an existing candidate intact. With the official instance configured and running, launch one run:

```bash
uv run python -m career_sim_runner play --submission solution-v4.3
```

Retain the resulting events, transcript and score report. Keep credentials in the participation repository's local `.env`; they are not part of this package.

## Final submission

Add the English team video as `presentation.mp4` inside this directory, update it to describe v4.3, and run the official validator:

```bash
uv run python -m career_sim_runner validate --submission solution-v4.3
```

For submission, name the completed directory `solution` and ZIP it as the sole archive root. The supplied development archive has that root but does not yet contain the presentation.
