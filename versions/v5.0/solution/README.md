# Spärk AI Career Survival Agent

Version: `career-survival-uk-v5.0-adaptive-policy`

The agent develops a career across 48 months by assessing current choices, protecting against credible failure and investing in sustained advancement. It uses one JiuwenSwarm 0.2.4b3 agent with two Skills.

| Skill | Responsibility |
| --- | --- |
| `career-controller` | Monthly decisions, review feedback, action verification, concise context and recovery. |
| `quarterly-planning` | Remaining Energy, main-action selection, competing needs and benefit timing. |

The policy uses the public handbook and evidence returned during the current run. It compares the costs and safeguards of available choices, matches corrective actions to the concern, and revises its plan when feedback changes. Every action is followed by an observation before another action is selected.

The manifest retains the core procedure across context recovery. The Skills supply the decision criteria. No runtime scripts or reference files are required.

Development status: structural checks and synthetic scenario review are recorded separately from simulation results. This version has not yet completed a run with the designated competition model.

The final submission must include the team's English `presentation.mp4`, at its original playback speed and no longer than ten minutes.
