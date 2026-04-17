# Implementing GitHub Copilot in Engineering Teams
## Shared setup, workflow, and guardrails

---

## How to use this document

This document is a reusable working draft for a presentation about GitHub Copilot and Copilot CLI.

It is designed to be:
- generic enough to reuse in other projects
- practical enough to apply to a real repository
- simple enough for a Spanish-speaking audience using English at work

This version assumes:
- the repository has no AI setup yet
- the organization wants a real rollout path
- the team already uses, or plans to use, GitHub Copilot CLI

The structure includes:
- presentation title
- presentation goal
- 13-slide deck outline
- presenter notes
- 2 demo sections
- recommended repo baseline
- rollout checklist
- appendix on Copilot, Codex, and Claude
- source appendix for validation work

---

## Recommended presentation title

**Implementing GitHub Copilot in Engineering Teams**  
**Shared setup, workflow, and guardrails**

Alternative titles:
- **Working Better with GitHub Copilot**
- **A Practical GitHub Copilot Setup**
- **GitHub Copilot for Teams**

Recommended file name:
`using-github-copilot-well-team-rollout`

---

## Presentation goal

The goal of this presentation is not to show every Copilot feature.

The goal is to explain:
1. what GitHub Copilot and Copilot CLI are
2. what the organization can control
3. what the repository must define
4. how a team should use Copilot in a shared and safe way
5. what changes if other AI tools are also allowed
6. what the next rollout steps should be

---

# 13-slide presentation structure

---

## Slide 1. Why we need a shared AI setup

### Slide title
**Why we need a shared AI setup**

### Slide text
- AI is already used in development.
- Today, we do not have one common standard.
- Our goal is simple: more speed, more quality, more control.

### Presenter notes
This slide should frame the talk.

The message is:
we do not need more AI chaos. We need one shared way of working.

Do not start with features.
Start with the operating model.

Suggested speaking notes:

> AI is already part of development work. The real question is not whether we use it. The real question is how we use it as a team. If we do not define one shared setup, each person will use AI in a different way, and that creates noise, inconsistency, and unnecessary risk.

---

## Slide 2. What GitHub Copilot and Copilot CLI are

### Slide title
**What GitHub Copilot and Copilot CLI are**

### Slide text
- GitHub Copilot helps with coding tasks across suggestions, chat, reviews, and agent workflows.
- Copilot CLI is the terminal version.
- In Copilot CLI, repository instruction files become part of the working context.

### Presenter notes
Keep this simple.
The point is not to explain every product surface.
The point is to show that Copilot is not only autocomplete.

Suggested speaking notes:

> GitHub Copilot is more than code completion. It can help through chat, code review, and agent-style workflows. Copilot CLI brings that experience into the terminal. In CLI, context matters a lot, and repository instruction files are part of that context.

---

## Slide 3. Three control layers

### Slide title
**Three control layers**

### Slide text
- Organization
- Repository
- Local tool and user environment

### Presenter notes
This is a very important slide.
It prevents a common mistake: thinking that organization setup controls everything.
It does not.

Suggested speaking notes:

> To govern AI well, we need to separate three layers. The organization controls access and policies. The repository controls shared instructions and workflow guidance. The local tool and user environment still matter, especially if people also use other AI tools outside Copilot.

---

## Slide 4. What the organization can control

### Slide title
**What the organization can control**

### Slide text
- The organization can control access, policies, features, and models.
- Enterprise policies can override organization settings.
- The organization can also review usage and adoption metrics.

### Presenter notes
This is the governance slide.
Make it clear that this is where shared access and shared visibility start.

Suggested speaking notes:

> At organization level, we can decide who gets access, which features are available, which models are allowed, and how we track adoption. This is the right place to define shared governance. But this still does not define how Copilot CLI behaves inside a repository.

---

## Slide 5. What the repository can control from day one

### Slide title
**What the repository can control from day one**

### Slide text
- `.github/copilot-instructions.md` for repository-wide rules
- `.github/instructions/*.instructions.md` for path-specific rules
- `AGENTS.md` for agent guidance
- These files are read automatically by Copilot CLI in that repository

### Presenter notes
This is where the practical setup starts.
This slide shows the minimum real foundation for shared CLI behavior.

Suggested speaking notes:

> If we want shared behavior in Copilot CLI, the repository must define it. The core files are repository-wide instructions, path-specific instructions, and optional agent guidance. These are the files that make Copilot behave more like our team expects.

---

## Slide 6. Our minimum setup for a repo with no AI configuration

### Slide title
**Our minimum setup for a repo with no AI configuration**

### Slide text
- Start with one small `.github/copilot-instructions.md`
- Put build and test commands there
- Add code style, required checks, and architecture rules
- Add path-specific files only where needed
- Keep instructions short, clear, and specific

### Presenter notes
Do not make this look heavy.
This is meant to feel realistic and easy to start.

Suggested speaking notes:

> The right first step is a small baseline, not a large rule book. We should start with the commands and rules that matter most: how to build, how to test, how to verify work, and the main architecture expectations. Then we add path-specific instructions only where they really help.

---

## Slide 7. Demo 1: initialize the repo baseline

### Slide title
**Demo 1: initialize the repo baseline**

### Slide text
- Create `.github/copilot-instructions.md`
- Add one small `backend.instructions.md`
- Ask Copilot CLI a repository question
- Show that it uses the instructions automatically

### Presenter notes
This is the first demo.
Its purpose is not to impress.
Its purpose is to prove that shared repository instructions change behavior from day one.

Suggested speaking notes:

> This first demo is intentionally simple. We are not showing complex generation. We are showing that even a small baseline changes how Copilot CLI answers and works inside the repo.

---

## Slide 8. The team workflow we should standardize

### Slide title
**The team workflow we should standardize**

### Slide text
- Explore first
- Use `/plan` for complex work
- Implement in small changes
- Verify before PR
- Reset the session when tasks are unrelated

### Presenter notes
This is one of the most important slides in the deck.
The real value is the method, not only the tool.

Suggested speaking notes:

> The main improvement will not come only from configuration. It will come from one shared workflow. We should explore first, plan before complex work, implement in smaller steps, verify before opening a pull request, and reset context when tasks are unrelated.

---

## Slide 9. Quality, security, and real limits

### Slide title
**Quality, security, and real limits**

### Slide text
- Require pull requests and review
- Require tests before merge
- Review AI changes before accepting
- Do not rely on content exclusion for Copilot CLI

### Presenter notes
This slide must sound serious and realistic.
Do not oversell control.
Do not say content exclusion solves CLI risk, because it does not.

Suggested speaking notes:

> Copilot can improve speed, but we still need normal engineering control. Pull requests, reviews, and tests remain necessary. Also, one important limitation is that content exclusion does not apply to Copilot CLI, so we should not present it as a CLI control.

---

## Slide 10. Can we also allow Codex or Claude?

### Slide title
**Can we also allow Codex or Claude?**

### Slide text
- Yes, but this is a governance choice, not only a user choice.
- On GitHub, OpenAI Codex and Anthropic Claude can be enabled as third-party coding agents.
- These GitHub third-party agents work asynchronously on issues and pull requests.
- They are in public preview.

### Presenter notes
Keep this balanced.
Do not say no by default.
Do not say yes without conditions.

Suggested speaking notes:

> It is possible to allow Codex or Claude in some GitHub workflows, but that should be treated as a governance decision. On GitHub, third-party agents can work asynchronously on issues and pull requests. That is different from letting people use local tools with their own config and permissions in any way they want.

---

## Slide 11. What changes when we mix many AI tools

### Slide title
**What changes when we mix many AI tools**

### Slide text
- We will have more than one instruction system
- We will have more than one permissions model
- We will have more than one configuration path
- This can create drift and confusion

### Presenter notes
This is the practical risk slide.
The message is not “other tools are bad”.
The message is “more tools mean more governance work”.

Suggested speaking notes:

> Mixing tools is possible, but then we are no longer managing one shared setup. We are managing more than one instruction system, more than one permissions model, and more than one rollout path. That increases the chance of drift and confusion, especially at the start.

---

## Slide 12. Demo 2: show the standard workflow

### Slide title
**Demo 2: show the standard workflow**

### Slide text
- Start with `/plan`
- Review the plan
- Run one small implementation step
- Ask for verification before PR

### Presenter notes
This demo should show the method.
It should not try to show a huge feature.

Suggested speaking notes:

> This second demo shows the workflow we want the team to remember. Plan first, then implement one step, then verify before moving forward. That is the repeatable pattern we want to standardize.

---

## Slide 13. Recommendation and next steps

### Slide title
**Recommendation and next steps**

### Slide text
- Standardize GitHub Copilot and Copilot CLI first
- Add repository instructions in the pilot repos
- Train the team on `/plan`, review, and validation
- Track usage and feedback
- Review later if we need Codex or Claude in controlled cases

### Presenter notes
End with a concrete recommendation.
Make it feel like a rollout plan, not a theoretical conclusion.

Suggested speaking notes:

> Our recommendation is to standardize Copilot first, create a small shared baseline at repository level, train the team on the workflow, and track real usage. After that, if we still see a clear need, we can review controlled use of other tools.

---

# Demo section

## Demo 1. Initialize the repo baseline

### Goal
Show that a repository with no AI setup can gain immediate structure with a small shared baseline.

### Recommended setup before the demo
Create these files:

```text
.github/copilot-instructions.md
.github/instructions/backend.instructions.md
```

### Suggested content for `.github/copilot-instructions.md`

```md
# Repository instructions

- Always explain the plan before large changes.
- Use the existing project structure and naming conventions.
- Before proposing code changes, identify the main files involved.
- After code changes, explain how to verify the result.
- Prefer small, reviewable changes over large rewrites.
- Use the project's standard test and lint commands before finalizing work.
```

### Suggested content for `backend.instructions.md`

```md
---
applyTo: "src/backend/**/*.ts,src/api/**/*.ts"
---

# Backend instructions

- Follow the current service and controller patterns.
- Do not introduce new frameworks.
- Reuse validation and error handling patterns already present in the codebase.
- If a change affects an API contract, call it out clearly.
```

### Suggested CLI prompt

```text
Read the repository rules first.
Then explain how you should work before changing the authentication code.
Do not write code yet.
```

### What to explain after the demo
- The repository now has a shared AI baseline.
- The AI behavior is more consistent.
- The team no longer depends only on prompt quality.
- The repository itself carries part of the working rules.

---

## Demo 2. Show the standard workflow

### Goal
Show the recommended working pattern for complex tasks.

### Suggested CLI prompt

```text
/plan Add validation to the login form and update the related tests
```

Then continue with:

```text
Proceed with step 1 only.
After that, run the relevant tests and explain any failures.
```

### What to explain after the demo
- We start with planning.
- We review the proposed steps.
- We implement one small step.
- We ask for validation before moving on.
- This creates a safer and more repeatable workflow.

---

# Suggested starter files for a repository with no AI setup

## File 1. `.github/copilot-instructions.md`

```md
# Copilot instructions

## How to work in this repository
- Start by understanding the relevant files before proposing changes.
- For complex tasks, explain a plan before writing code.
- Prefer small and reviewable changes.
- Reuse existing patterns before creating new ones.
- Explain how to validate the proposed change.

## Quality rules
- Respect the current architecture and folder structure.
- Follow the existing naming conventions.
- Do not change unrelated files.
- Call out assumptions and risks clearly.

## Verification
- Suggest the relevant tests for the change.
- Mention lint or build checks when relevant.
```

## File 2. `.github/instructions/backend.instructions.md`

```md
---
applyTo: "src/backend/**/*.ts,src/api/**/*.ts"
---

# Backend rules
- Use existing controllers, services, and validation patterns.
- Keep API changes explicit.
- Avoid large refactors unless requested.
- Keep changes small and easy to review.
```

## File 3. `.github/instructions/frontend.instructions.md`

```md
---
applyTo: "src/frontend/**/*.ts,src/frontend/**/*.tsx,src/ui/**/*.tsx"
---

# Frontend rules
- Reuse existing UI components and styling patterns.
- Keep state changes simple and predictable.
- Avoid unnecessary visual changes.
- If a change affects UX, explain it clearly.
```

## File 4. `AGENTS.md`

```md
# Agent guidance

- Read repository instructions before proposing changes.
- For complex work, suggest a plan first.
- Keep changes focused and easy to review.
- Explain verification steps before finalizing.
- Raise risks, assumptions, and open questions clearly.
```

---

# Recommended rollout path

## Phase 1. Organization baseline
- Enable GitHub Copilot for the right teams first.
- Review organization policies, features, and model access.
- Confirm who will own rollout, governance, and reporting.

## Phase 2. Repository baseline
- Add `.github/copilot-instructions.md` to pilot repositories.
- Add path-specific instruction files only where useful.
- Add `AGENTS.md` if the team will use more agent-style CLI workflows.

## Phase 3. Team workflow
- Teach the team to use `/plan` for complex tasks.
- Align on review, verification, and PR expectations.
- Ask people to keep sessions focused.

## Phase 4. Adoption review
- Review usage and adoption metrics.
- Collect team feedback.
- Improve instructions where results are unclear.

## Phase 5. Controlled expansion
- Review whether other AI tools are still needed.
- If yes, define governance before enabling them broadly.
- Keep Copilot as the shared base unless there is a strong reason not to.

---

# Should the presentation be generic or project-specific?

## Recommendation
Use a **generic base presentation** with **small project-specific touches**.

## Best balance
- 80% generic
- 20% adapted

## Keep generic
- what Copilot is
- control layers
- organization vs repository setup
- workflow
- guardrails
- multi-tool policy
- next steps

## Adapt when needed
- repo folder names in examples
- one real example in Demo 1
- one real example in Demo 2
- next steps for the current repository

This keeps the deck reusable while still making it feel relevant.

---

# Appendix: Copilot, Codex, and Claude

## GitHub Copilot and Copilot CLI
Use this as the standard first layer when the organization wants:
- one main governance path
- one main adoption path
- one main metrics path
- shared repository instructions

## Codex or Claude on GitHub
These can be considered later for controlled cases where the organization wants third-party coding agents working through GitHub workflows.

Important practical message for the presentation:
- allowing them is possible
- allowing them is not the same as standardizing them
- they should be treated as a later governance decision

## Local tools outside the GitHub control path
If people use local tools, the organization must assume:
- different configuration files
- different permissions models
- different approval flows
- more operational drift

That does not automatically mean “do not allow them”.
It means “do not confuse them with one shared governed standard”.

---

# Source validation appendix

This section is for your own notes, not for slide text.

Key points used in this document were checked against official documentation from:
- GitHub Docs for organization setup, Copilot CLI best practices, repository custom instructions, content exclusion, metrics, and third-party agents
- OpenAI Codex documentation for `AGENTS.md` and Codex configuration patterns
- Anthropic Claude Code documentation for local configuration and permission models

## Main facts that should remain explicit in the presentation

1. **Organization custom instructions do not cover Copilot CLI.**
   GitHub documents organization custom instructions for some GitHub.com surfaces, not Copilot CLI.

2. **Content exclusion does not support Copilot CLI.**
   GitHub explicitly says Copilot CLI is not covered by content exclusion.

3. **GitHub can enable Codex and Claude as third-party agents on GitHub, but that does not govern local tools.**
   GitHub also says those policies do not apply to local agents in Visual Studio Code.

4. **Repository instruction files are the real baseline for Copilot CLI behavior.**
   That is why the repository baseline is central to the rollout plan.

---

# Final recommendation

If you need one clear message for the presentation, use this:

**First standardize GitHub Copilot and Copilot CLI with a small repository baseline and a shared team workflow. Then review whether other AI tools are needed in controlled cases.**

That is the most practical, reusable, and defensible approach for a team starting from zero.
