# Skill architecture

## Objective and execution model

Spärk AI uses one JiuwenSwarm 0.2.4b3 agent to complete the 48-month career simulation while developing career level, wealth, capability and relationships. Health, dignity and organisational risk constrain that development. The design separates continuous decision control from quarterly resource planning without introducing additional agents.

## Responsibilities

| Skill | Responsibility | Decision output |
|---|---|---|
| Career controller | Session continuity, story choices, review interpretation, warning tracking, action verification and recovery | One choice from the current menu, with a short rationale |
| Quarterly planning | Remaining Energy, published costs, main-action alternatives and current career needs | The next feasible step of a provisional allocation |

The controller owns simulation interaction. During a quarterly phase it applies the planner's procedure, executes one action and checks the resulting observation before committing further resources. The main action is assessed alongside the allocation but kept separate from Energy spending.

## Information flow

The agent reads the public employee handbook and uses the official MCP tools: `new_game`, `observe`, `take_action`, `check_latest_logs` and `show_employee_handbook`. Current observations supply the phase, available choices, visible state and feedback. Public descriptions and exposed costs support comparison; undisclosed effects remain uncertain.

The execution sequence is:

1. Observe the current state and menu.
2. Verify the preceding action's result.
3. Identify the most pressing supported objective.
4. Select and execute one feasible choice with a brief decision note.
5. Inspect the next observation and revise the objective as needed.

The agent reads each relevant Skill before using it and reloads instructions after context loss. Notes record the decisive evidence, intended benefit and accepted cost rather than repeating the session history.

## Working state

The agent retains the session and phase, current objective, latest review, unresolved warnings and commitments, and the last relevant action and observed result. Current observations replace stale values. A concern retains its source, attempted response and latest evidence until feedback supports reducing its priority.

Action acceptance, expected benefit and observed change are distinct. Salary, reviews and intervening events can affect the next observation, so a net change is not automatically attributed to one action. Missing benefits trigger comparison with a feasible alternative and, where useful, a targeted check of recent official logs.

## Risk and development

An organisational incident or persistent or escalating warnings make relevant mitigation take priority over optional growth that adds exposure. Another immediate survival threat can take precedence. Rebuilding Output is tracked separately from repairing the underlying concern; strong statistics or promotion do not clear a risk warning.

Each quarter compares growth, recovery and mitigation against current needs and remaining resources. The agent checks the result of mitigation before deciding whether to repeat it. Improving evidence allows renewed investment in development. This avoids both automatic growth bundles and indefinite defensive spending.

Output supports performance and advancement. Ending decisions also consider directly scored dimensions and the remaining opportunities for promotion. No private promotion threshold or fixed action schedule is embedded in the Skills.

## Recovery and implementation

After an uncertain action, the controller reconciles the current observation and recent official logs before retrying. It preserves the existing session and reports an unresolved interface problem rather than duplicating an action or restarting the game. The official ending determines completion.

Markdown Skills express the policy; the official MCP tools provide execution and recovery. Additional scripts and reference files would duplicate those responsibilities without adding a required capability. Working memory stays in the session context.

The same procedures apply to changed event wording, ordering and available choices: decisions depend on the current menu, published costs and observed feedback rather than stored answers. The principal operational risks are missed warnings, stale context, incorrect attribution and repetitive reasoning. Compact state, one-action execution and explicit verification address these risks.
