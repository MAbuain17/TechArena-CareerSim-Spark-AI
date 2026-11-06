# Spärk AI Career Survival Agent

Version: `career-survival-uk-v5.1-evidence-priorities`

One JiuwenSwarm 0.2.4b3 agent uses two Markdown Skills to develop a career across 48 months. The career controller handles monthly choices, feedback, action verification and context recovery. The quarterly planner allocates Energy and compares main actions.

The agent keeps unresolved survival concerns active across decisions. Financial distress and organisational warnings take priority over discretionary commitments unless observed recovery or a more urgent competing threat supports a different choice. Once those concerns are addressed, the agent invests in sustained advancement and the ending dimensions.

Every action uses the current menu and is followed by observation. Compact notes retain the current objective, supporting evidence, attempted remedies and the next condition to check. The policy uses public rules and current-run feedback, without fixed event answers or hidden thresholds.

Version 5.1 addresses the trust-crisis and financial failures observed in two v5.0 development runs. Its score has not yet been measured in a complete designated-model run.

Keep the previous candidate separately. Place this package's `solution` folder inside `candidate-v5.1` under the official repository. For one local run with the server running:

```powershell
uv run python -m career_sim_runner play --submission ".\candidate-v5.1\solution"
```

Before final submission, add the team's English `presentation.mp4` inside `solution/`. It must use original playback speed and be no longer than ten minutes. The archive supplied for local testing does not include that video.
