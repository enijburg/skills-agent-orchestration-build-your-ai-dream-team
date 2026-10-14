# Agent team

I will use GitHub Copilot CLI in a Codespace to orchestrate the team building Mona's Project Pulse dashboard.

| Agent | Model | Responsibility | Definition |
|---|---|---|---|
| Orchestrator | Claude Opus 4.7 (copilot) | Coordinates the work, delegates tasks to specialists with clear file ownership, manages phases and dependencies, and verifies and reports the integrated result. | `.github/agents/orchestrator.agent.md` |
| Planner | Claude Opus 4.7 (copilot) | Researches the project and creates an implementation plan with steps, file assignments, dependencies, parallel work, edge cases, and validation expectations. | `.github/agents/planner.agent.md` |
| Designer | Gemini 3.1 Pro (copilot) | Guides the dashboard's usability, accessibility, information hierarchy, interaction flow, responsive behavior, and visual design. | `.github/agents/designer.agent.md` |
| Coder | GPT-5.5 (copilot) | Implements and validates assigned code, following project patterns and keeping behavior clear, deterministic, and testable. | `.github/agents/coder.agent.md` |

The Orchestrator will first ask the Planner to map the Project Pulse work into phases and assign files. The Designer will guide the dashboard experience while the Coder implements the static app. The Orchestrator will coordinate dependencies, integrate the work, and verify the finished dashboard.
