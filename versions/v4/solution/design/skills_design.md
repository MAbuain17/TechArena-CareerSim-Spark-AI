# Skill architecture

## Execution model

A single JiuwenSwarm agent executes both Skills within one simulation session. `career-controller` owns the decision loop and all simulation actions. `quarterly-planning` supplies the allocation procedure during quarterly phases. The controller applies the selected action, observes its result and updates the plan.

## Responsibilities

The controller establishes or resumes the session, reads the current state and offered choices, evaluates story decisions, and submits one action at a time. It reconciles uncertain execution before retrying and continues until the interface returns the official ending.

The quarterly planner evaluates the remaining Energy budget, available actions, current vulnerabilities and review feedback. It compares feasible allocations and selects the next step of a provisional plan. The main action is assessed against the same career objectives. Each subsequent observation can change the remaining allocation.

## State and feedback

Working state contains the session and phase, current objective, latest review, unresolved warnings and commitments, and relevant recent action outcomes. Current observations replace stale numerical values. Open concerns retain their source, attempted response and latest evidence until feedback supports closing them.

Outcome verification separates the intended effect, successful action acceptance and observed result. Salary, reviews and intervening events are considered before attributing a statistical change to one action. Missing gains trigger reassessment and targeted log retrieval where clarification is useful.

Performance and organisational risk are tracked separately. Strong visible statistics do not close an unresolved warning. A mitigation action records a response; subsequent feedback determines whether further work is needed.

## Implementation choices

The Skills contain the decision procedures in Markdown. The official MCP interface supplies the observation, action and recovery functions, so the design requires no additional runtime scripts or reference service. Session recovery uses current observations and recent official logs.

Action notes retain the decisive evidence, expected benefit and material cost. This keeps the working context focused on information needed for later decisions.

## V4 execution changes

V4 checks the preceding outcome before selecting the next action. It requires comparison with an alternative before repeating an action for an absent benefit, and checks affordable opportunities before leaving Energy unused. Quarterly planning considers Energy spending and the main action together, including intermediate safety and outstanding risk concerns.

The controller reuses loaded instructions while available and retrieves logs to resolve specific questions. Shorter notes reduce repeated history while preserving unresolved commitments and feedback.
