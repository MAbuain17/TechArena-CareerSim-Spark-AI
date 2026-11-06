# Spärk AI Career Survival Agent

Version: career-survival-uk-v6.0-joint-allocation

One agent uses six Skills: session-state, choice-evaluation, survival-response, quarterly-portfolio, advancement-strategy and finish-and-score. The objective is a strong 48-month career outcome through sustained advancement, effective resource allocation and timely correction of failure risks.

The quarterly planner compares Energy and main actions together. Monthly decisions evaluate practical consequences, recurring commitments and available safeguards. Review feedback directs development; remaining time determines whether delayed investments are worthwhile.

This version has not completed a designated-model run. Structural validation does not establish a performance improvement.

Keep previous versions separately. Extract this archive under candidate-v6 in the official repository. With the official server running, local play is:

```powershell
uv run python -m career_sim_runner play --submission ".\candidate-v6\solution"
```

For final submission add the team's English presentation.mp4, at original speed and at most ten minutes, inside solution. Then validate and zip the solution folder:

```powershell
uv run python -m career_sim_runner validate --submission ".\candidate-v6\solution"
```

No video is included in this package. Do not submit it without adding the required presentation.
