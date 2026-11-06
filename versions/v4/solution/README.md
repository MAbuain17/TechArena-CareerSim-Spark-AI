# Spärk AI V4: Career Survival Agent

Spärk AI uses one JiuwenSwarm agent to manage the 48-month career simulation. Two Skills structure its decisions: `career-controller` manages the session, story choices, feedback and completion; `quarterly-planning` manages Energy allocation and the quarterly main action.

The agent pursues career advancement and financial resilience while maintaining health, dignity, professional capability, relationships and risk control. It selects actions from the current official menu and checks subsequent observations against the intended result.

## Runtime

JiuwenSwarm 0.2.4b3 in `agent` mode, using the organiser-designated model and routing. Simulation access uses the five official MCP tools: `new_game`, `observe`, `take_action`, `check_latest_logs` and `show_employee_handbook`.

## Design documents

`design/skills_design.md` describes Skill responsibilities, state management and execution. `design/decision_report.md` explains the decision policy, development findings and validation status.
