# Implementing GitHub Copilot in Engineering Teams
## Shared setup, workflow, and guardrails

---

## How to use this document

This document is a working draft for a rollout presentation about GitHub Copilot and Copilot CLI.

It is designed to be:
- practical for a technical team
- grounded in a real frontend and backend workspace
- anonymous enough to avoid exposing private project details
- simple enough for a Spanish-speaking audience using English at work

This version assumes:
- the team already works with two coordinated repositories from one parent workspace
- the minimum Copilot baseline is already configured in the real repositories
- `/.github/copilot-instructions.md` exists in both frontend and backend
- `AGENTS.md` exists as complementary guidance
- the audience already uses Copilot, but not always well
- the examples should be derived from a real project shape without naming the product

The structure includes:
- presentation title
- presentation goal
- 14-slide deck outline
- presenter notes
- 2 demo sections
- recommended repository baseline
- rollout checklist
- guidance on Copilot Enterprise, AGENTS, and mixed AI tools

---

## Presentation goal

The goal of this presentation is not to show every Copilot feature.

The goal is to explain:
1. why the team needs one shared AI operating model
2. how Copilot Enterprise and repository setup shape behavior
3. how to stop using Copilot poorly in day-to-day work
4. how to prompt and steer Copilot CLI well
5. how to use planning, review, skills, agents, and subagents with intent
6. how to keep quality and guardrails intact
7. what the next rollout steps should be

---

# 14-slide presentation structure

---

## Slide 1. Why this needs a shared AI operating model

### Slide title
**Why this needs a shared AI operating model**

### Slide text
- `The problem is not access. The problem is using Copilot with one shared standard.`
- AI is already part of development work.
- Many teams already use Copilot, but not always in the same way.
- Without one shared model, AI adoption creates drift, review noise, and uneven quality.

### Presenter notes
This slide should frame the talk around behavior, not tooling alone.

### Animation / Design
- Use an editorial split layout.
- Put the title block on the left and the explanatory copy on the right.
- Keep the left side visually dominant, but let the right side carry the practical framing.
- Above the bullets, include one short intro sentence:
  - `The problem is not access. The problem is using Copilot with one shared standard.`
- Reveal the title first, then the intro, then the bullets with a short staggered entrance.
- Keep the motion restrained and avoid decorative diagrams.

Suggested speaking notes:

> AI is already part of development work. The question now is not access. The question is how we use it well as a team. If each person uses Copilot with a different approach, we get drift, review noise, and inconsistent quality. What we need is one shared way of working.

---

## Slide 2. How Copilot works in practice

### Slide title
**How Copilot works in practice**

### Slide text
- Copilot is not only autocomplete.
- It works through context, instructions, policies, and workflow.
- The result depends on the environment we create around it.

### Presenter notes
Keep this practical and not product-marketing.

### Animation / Design
- Use a split 50/50 layout.
- Put the visual on the left and the text on the right.
- The left side should use a real-looking coding scene, not a diagram.
- Recommended visual: an editor with a short inline suggestion and a minimal terminal footer.
- The coding example should feel like a real task flow, not a fake product mockup.
- A good example is a small validation flow with an inline completion and a subtle Copilot CLI command in the terminal.
- The image should feel real and legible at a glance, without too much small text or decorative UI.
- Avoid admin settings, dashboards, or configuration screens.
- Animate the image first with a soft fade-in.
- Then reveal the text on the right with a short staggered entrance.
- Keep the motion clean and restrained.
- Add a short closing note under the bullets:
  - `Rollout is not one switch. It is a system we shape on purpose.`

Suggested speaking notes:

> Copilot is not only autocomplete. In practice, it works through the context it sees, the instructions it receives, the policies that enable or disable features, and the workflow we expect people to follow. The result depends on the environment we create around it. So rollout is not one switch. It is a system we shape on purpose.

---

## Slide 3. Three control layers

### Slide title
**Three control layers**

### Slide text
- `Rollout only works when these three layers reinforce each other.`
- `Enterprise / organization` — `policy and access`
- `Repository` — `shared rules`
- `Local tool and user environment` — `execution context`

### Presenter notes
This slide explains why rollout is never only an admin setting.

### Animation / Design
- Do not use a 50/50 layout.
- Use a centered editorial composition.
- Put the title and one short framing sentence at the top center.
- Below, use three horizontal blocks aligned in one row:
  - `Enterprise / organization`
  - `Repository`
  - `Local tool and user environment`
- Each block should include a short function label:
  - `policy and access`
  - `shared rules`
  - `execution context`
- The three blocks should feel like one system, not three unrelated cards.
- Keep the motion minimal: title first, framing sentence second, then the three blocks.
- This slide should prepare Slide 4 as a zoom into the enterprise layer.

Suggested speaking notes:

> We need to separate three layers. Enterprise or organization controls policy and access. The repository controls shared engineering rules. The local tool and user environment matter because that is where execution happens. This layered view helps us see what belongs to governance, what belongs to the repo, and what depends on daily usage.

---

## Slide 4. What Enterprise and the organization control

### Slide title
**What Enterprise and the organization control**

### Slide text
- `Enterprise / Organization AI Controls`
- `Access` — `seat assignment and org-level delegation`
- `Policies & models` — `feature, privacy, and model controls`
- `GitHub-native AI surfaces` — `cloud agent, code review, MCP`
- `Visibility` — `metrics dashboards and APIs`
- `set centrally or delegated to organization owners`

### Presenter notes
This slide should work as a control map, not as a feature list or an admin slide.

It should be grounded in GitHub Docs:
- enterprise owners can define policies centrally or delegate decisions to organization owners
- Copilot policies are grouped into feature, privacy, and models
- AI controls include Copilot, agents, and MCP
- usage metrics provide visibility, but not with full coverage across every surface

### Animation / Design
- Do not use a 50/50 layout.
- Use a full-slide visual map with one central control node and four surrounding domains.
- Central node: `Enterprise / Organization AI Controls`
- Surrounding domains:
  - `Access`
  - `Policies & models`
  - `GitHub-native AI surfaces`
  - `Visibility`
- Each domain should use one real example of what is controlled:
  - `seat assignment and org-level delegation`
  - `feature, privacy, and model controls`
  - `cloud agent, code review, MCP`
  - `metrics dashboards and APIs`
- Add one small location hint inside each domain or as microcopy where useful:
  - `AI controls`
  - `Policies / Models`
  - `Agents / MCP`
  - `Dashboard / API`
- Add one small governance note:
  - `set centrally or delegated to organization owners`
- Do not use settings screens, admin pages, or dashboard screenshots.
- The slide should feel like a system map of control surfaces, not a feature list or abstract diagram.
- Keep the title compact and secondary to the map.
- Use a centered and symmetric composition: central node in the middle, four domains in a square around it.
- Keep connectors minimal and only if they improve readability.
- Animate the central node first, then reveal the four domains around it.

Suggested speaking notes:

> At enterprise and organization level, GitHub gives us a real control surface. We can manage access, define policies, control model availability, and decide which GitHub-native AI capabilities are allowed. In GitHub Docs, this lives under AI controls, including Policies, Models, Agents, MCP, and metrics. Enterprise owners can define policies centrally or delegate them to organization owners. Policies are grouped into feature, privacy, and models. Cloud agent and MCP are controlled in the AI controls area, and usage visibility comes from dashboards and APIs. That visibility is useful, but it is not complete across every surface. So this layer matters, but it defines the operating envelope more than the day-to-day engineering workflow.

---

## Slide 5. What an AI repo setup looks like

### Slide title
**What an AI repo setup looks like**

### Slide text
- Two real repositories coordinated from one parent workspace
- Repository-wide Copilot baseline already configured
- `AGENTS.md` is useful as complementary guidance

### Presenter notes
This is where the case study becomes concrete.

Suggested speaking notes:

> In our case, our working workspace has a frontend repository and a backend repository. The Copilot baseline lives in the real repositories where the code and Git history live. Repository-wide copilot-instructions.md gives the most portable Copilot baseline, and AGENTS.md helps, especially for agent workflows.

---

## Slide 6. What each repository must define

### Slide title
**What each repository must define**

### Slide text
- Shared rules for the code it owns
- Contract ownership with the other side
- Real verification commands and quality expectations

### Presenter notes
Keep this centered on engineering reality.

Suggested speaking notes:

> Even with Enterprise in place, each repository needs to define the rules that matter in that codebase. That includes its architecture, how contracts are owned, and how changes are validated. This is where Copilot becomes project-aware instead of generic.

---

## Slide 7. Bad prompts vs good prompts

### Slide title
**Bad prompts vs good prompts**

### Slide text
- `Bad prompting`
- Vague ask
- Too much scope
- No success criteria
- No verification
- No ownership boundary
- `Good prompting`
- Clear goal
- Relevant context
- Constraints and limits
- Expected output
- One small next step

### Presenter notes
This slide should open the practical block through contrast, not through two separate explanations.

Suggested speaking notes:

> On the left is the pattern that usually produces weak results. The ask is vague, the scope is too large, there is no clear success criteria, no verification step, and no ownership boundary. On the right is the same task shaped properly. The goal is clear, the relevant context is included, constraints are explicit, the expected output is defined, and the next step is small enough to execute well. The point is simple: the tool usually reflects the shape of the task we give it.

### Animation / Design
- Do not split this into two separate slides.
- Use one full-width comparison slide.
- Left side:
  - `Bad prompting`
  - visually heavier, less stable, slightly uncomfortable
- Right side:
  - `Good prompting`
  - cleaner, calmer, more structured
- The comparison should read in 2-3 seconds without needing speaker notes.
- Prefer a paired comparison instead of two long unrelated lists.
- Do not make it a dense table.
- The slide should feel visual and direct.

---

## Slide 8. The CLI patterns and capabilities that matter daily

### Slide title
**The CLI patterns and capabilities that matter daily**

### Slide text
- Conversation
- `/plan`
- `/review`
- Skills
- Custom agents and subagents

### Presenter notes
This slide is the map of the practical CLI block.

Suggested speaking notes:

> We do not need to teach every CLI feature. We need to teach the few patterns and capabilities that change daily work. Normal conversation, planning, review, skills, and agent delegation are enough to improve most day-to-day tasks.

---

## Slide 9. Live demo 01 — Add a loading state to the login button

### Slide title
**Live demo 01: Add a loading state to the login button**

### Slide text
Two paths, same task. Login button gives no visual feedback on submit.

**Without /plan:**
- Direct prompt: "Add a loading state to the login button"
- Copilot infers context from the open file — no codebase inspection
- May duplicate patterns or miss the auth hook state

**With /plan + Socratic:**
- `/plan "Add a loading state to the login button"`
- Copilot inspects codebase: auth hook, button component, existing loading patterns
- Asks clarifying questions before writing — built-in behavior of /plan
- Waits for approval, then targeted implementation · execute one step · review

### Presenter notes
This is a live demo. Run both paths in the terminal. The audience should see the difference in what Copilot touches and asks.

Suggested speaking notes:

> We are going to run this demo live. The scenario is a login button with no visual feedback — the user clicks and nothing happens until the response comes back. We will run the same task twice: first with a direct prompt, then with /plan. With /plan, we also tell Copilot to ask if it has doubts before implementing — that is the Socratic mode. Watch how the plan changes what Copilot touches and what it leaves alone.

---

## Slide 10. How to use /review

### Slide title
**How to use /review**

### Design notes
Visual and minimalist. Command list layout — same pattern as slide 08.
Left column: command (code). Right column: what it does (muted text).
No bullets, no panels. Just commands and descriptions.

### Slide text — command list

| Command | What it does |
|---|---|
| `/diff` | see exactly what changed in the current directory |
| `/review` | analyze changes before committing — default criteria |
| `/review "focus on security"` | guided review with custom instructions |

### Workflow (speaker-facing, not on slide)
1. Make a change
2. `/diff` — see what changed
3. `/review` or `/review "focus on X"` — Copilot analyzes
4. Accept or decline its suggestions interactively
5. Implement feedback, then commit

### Presenter notes
Copilot should not be the last reviewer of its own work. /review gives quick feedback before you commit. You can guide it with a custom prompt — focus on security, contracts, or what was not tested.

Suggested speaking notes:

> After you implement something with /plan, run /review before you commit. No prompt needed — Copilot analyzes your changes by default. But you can guide it: focus on security, on contract changes, on what was not verified. The point is not speed alone. The point is controlled speed.

---

## Slide 11. Skills and custom agents

### Slide title
**Skills and custom agents**

### Design notes
50/50 split layout. Two columns, each a self-contained block.
Left block: Skills. Right block: Custom agents.
Each block has a label at the top, one or two commands in code style, a one-line description, and a muted "where it lives" path at the bottom.
No shared command list — two distinct visual units side by side.
Thin vertical divider between them.
Closing line below both columns: "Both live in the repository — the team shares them."

### Left block — Skills
Label: `skills`
Commands:
- `/skills list` — see what is available
- `/generate-tests "..."` — invoke by name

Description: repeatable instruction packages — define once, invoke anywhere
Where it lives: `.github/skills/SKILL.md`

### Right block — Custom agents
Label: `agents`
Commands:
- `/agent "..."` — open the agent selector
- `Use the security-auditor agent to check ...` — explicit invocation

Description: full personas — own tools, model, and behavioral scope
Where it lives: `.github/agents/<name>.agent.md`

### Presenter notes
Keep this concrete and anti-hype. Skills are instruction packages for repeatable tasks. Custom agents are full personas with their own tools, model, and scope.

Suggested speaking notes:

> Skills are repeatable instruction packages. You define them once and invoke them by name. Custom agents are fuller personas — they have their own tools, model configuration, and behavioral scope. Both live in the repository, which means the team shares them. Use them when a task is specialist enough to justify a dedicated pattern.

---

## Slide 12. Subagents

### Slide title
**Subagents — fleet and delegate**

### Design notes
Two large focal items, centered, stacked vertically with generous spacing.
No command-list table. Each item takes the full width with its command prominent and the description below it as a single muted line.
Think: editorial, sparse, one idea per visual unit.

Item 1:
- Command (large, code): `/fleet "..."`
- Description (muted, below): parallel subtasks — each agent runs in its own isolated context

Item 2:
- Command (large, code): `/delegate "..."`
- Description (muted, below): async cloud handoff — commits to a new branch, opens a draft PR

Closing line at the bottom, centered, very muted:
"Premium request cost scales with parallelism — use when the task justifies it."

### Presenter notes
These are the most powerful — and the most expensive in terms of premium requests. /fleet is for large decomposable tasks. /delegate is for async work you want to hand off completely.

Suggested speaking notes:

> /fleet breaks your task into independent subtasks and runs them in parallel, each with its own agent and context window. /delegate goes further — it hands the work off to the cloud agent entirely, which runs async, commits to a new branch, and opens a draft PR. Both are useful when the task is large and complex enough. Neither is something you use on every ticket.

---

## Slide 13. Demo 2: Agents and fleet

### Slide title
**Agents and fleet**

### Design notes
Same pattern as slide 09 (Demo 1 intro): SlideHeading with kicker + title, a brief setup block, and a closing "Let's try it." line.
The setup block shows two lines of context: the two agent files already in the repo, so the audience understands what exists before the demo runs.

Kicker: `Live demo 02`
Title: `Agents and fleet`

Setup block (muted, below title):
```
.github/agents/test-writer.agent.md
writes Jest + Supertest tests for a route

.github/agents/sql-reviewer.agent.md
reviews SQL in model files for injection risks
```

Closing line (large, same weight as slide 09):
`Let's fleet them.`

### Presenter notes
This demo has two parts: show the agent files exist in the repo, then run /fleet to delegate both tasks in parallel. The audience should see that agents are just markdown files — and that /fleet runs both simultaneously.

Suggested speaking notes:

> We have two agents already in the repo. One writes integration tests. The other reviews SQL for injection risks. Both are markdown files in .github/agents — the whole team has them. Now we run /fleet and delegate both tasks at the same time. Each agent runs in its own context. Neither one blocks the other.

---

# Demo section

## Demo 1. Add a loading state to the login button

### Goal
Show how `/plan` inspects the codebase, asks clarifying questions, and waits for approval before writing any code.

### Demo flow 01

Run:

```text
/plan The login submit button gives no visual feedback while user is awaiting. Add a loading state to the button during the request. Use socratic method to ask clarifying questions if needed.
```

Walk through what Copilot does:
- Inspects the codebase — finds `SubmitButton.jsx`, `LogIn.jsx`, existing patterns
- Asks clarifying questions if needed before writing
- Generates a plan — review it with the audience
- Approve and execute only the first step

### What to explain after the demo
- The prompt describes the problem and the context — not the solution.
- Copilot inspects before it writes — that is the key difference.
- The clarifying questions are not a delay — they are the inspection.
- Smaller, approved steps are easier to review and safer to merge.

---

## Demo 2. Agents and fleet on a real backend route

### Goal
Show how custom agents are just markdown files in the repo, and how `/fleet` delegates two independent tasks to them in parallel — without the presenter waiting for one to finish before starting the other.

### Setup (before the demo)
Two agent files already exist in `BIM2GO_backend/.github/agents/`:

- `test-writer.agent.md` — reads the existing test patterns in `test/`, then writes a Jest + Supertest integration test for the route under review.
- `sql-reviewer.agent.md` — reads a model file in `db/` and flags SQL queries that are not parameterized, classified as HIGH / MEDIUM / INFO.

Open both files briefly before running the demo — the audience should see that an agent is just a markdown file with a name, a tool list, and clear instructions.

### Demo flow

Step 1 — show the agent files:
```
cat .github/agents/test-writer.agent.md
cat .github/agents/sql-reviewer.agent.md
```
Point out: name, tools, instructions. "This is the whole agent."

Step 2 — run /fleet:
```
/fleet "Review db/card.model.js for SQL safety AND write integration tests for the card routes. Run both tasks in parallel."
```

Walk through what happens:
- Copilot spawns two agents simultaneously
- `sql-reviewer` reads `db/card.model.js` and reports findings (HIGH / MEDIUM / INFO)
- `test-writer` reads `routes/card.routes.js` + existing test patterns, writes `test/card.test.js`
- Both complete independently — no waiting

Step 3 — show the outputs:
- Review the SQL report: pick one HIGH or MEDIUM finding and explain it
- Open `test/card.test.js`: point out that it follows the project's existing patterns
- Run `npm test` to show the generated tests are valid

### What to explain after the demo
- The agents live in the repo — the whole team shares them from day one.
- `/fleet` is not magic. It is controlled parallelism with scoped agents.
- You define the agent once. You invoke it by name forever.
- The SQL reviewer finds what code review under time pressure misses.
- The test writer does not replace the engineer — it gives a starting point that already follows the project's patterns.

---

# Recommended repository baseline

## Repository-wide Copilot baseline

Use `/.github/copilot-instructions.md` inside each real repository.

This is the most portable baseline to present for Copilot because support is broader and easier to explain than more advanced instruction layers.

Suggested scope:
- working method
- architecture reminders
- contract rules
- verification commands
- hard limits

## Complementary agent guidance

Use `AGENTS.md` as a complementary layer, especially for agent workflows and CLI usage.

Position it as:
- useful
- valid
- already part of the real setup
- not a substitute for a clear repository-wide Copilot baseline

In this case, this means:
- backend keeps its existing `AGENTS.md` guidance
- frontend also has repository-level guidance instead of remaining empty
- the workspace-level `AGENTS.md` is routing guidance, not the main Copilot baseline

## Optional path-specific instructions

Use `.github/instructions/*.instructions.md` only where:
- the Copilot surface supports them
- the repository shape really benefits from them
- the extra complexity is justified

Do not make these files the center of the presentation.

## Precedence and support notes

- For supported Copilot surfaces, path-specific instructions in `.github/instructions/**/*.instructions.md` take precedence over `.github/copilot-instructions.md`.
- Repository-wide `.github/copilot-instructions.md` takes precedence over agent instruction files such as `AGENTS.md`.
- `AGENTS.md` is useful, especially for agent workflows, but it should not replace the repository-wide Copilot baseline in the presentation.
- Support is not identical across all Copilot surfaces. The safest baseline to present first is `.github/copilot-instructions.md` inside each real repository.

---

# Copilot CLI usage notes

## Bad prompts vs good prompts

Bad prompts usually fail because they:
- are vague
- ask for too much in one step
- omit verification
- omit ownership boundaries
- do not define success

Good prompts usually include:
- a clear goal
- relevant context
- constraints
- expected output
- one small next step

## The commands that matter most

The most useful day-to-day Copilot CLI patterns are:
- normal conversation for scoped questions
- `/plan` for complex or risky work
- `/review` for feedback before merge
- skills for repeatable specialist tasks
- custom agents and subagents for specialization or delegation

## How to explain skills, agents, and subagents

- Skills help Copilot perform specialized repeatable tasks.
- Custom agents let Copilot use a specialized role.
- Subagents let the main agent delegate part of the work.
- These are useful when the problem justifies them, not as a default for every task.

---

# Copilot Enterprise explanation notes

## What Enterprise changes

Copilot Enterprise or enterprise-level governance matters because it can control:
- access to Copilot
- enabled features
- model availability
- some GitHub-based agent capabilities
- code review and pull request summary features where enabled
- organization or enterprise-level usage visibility

## What Enterprise does not replace

Enterprise does not replace:
- repository architecture rules
- frontend and backend contract rules
- implementation conventions
- verification expectations
- prompt quality or task scoping

## How to explain this simply

Use this formula:

> Enterprise decides what is allowed and available.
> The repositories decide how Copilot should work in our code.
> The team workflow decides how we use it responsibly.

---

# Recommended rollout path

## Phase 1. Enterprise and organization baseline
- Confirm access, policies, enabled features, and model availability.
- Decide which GitHub-based agent capabilities are allowed.
- Review what usage data is actually available and where its coverage is limited.

## Phase 2. Repository baseline
- Keep repository-wide Copilot instructions in each real repository.
- Keep `AGENTS.md` where it adds value.
- Add path-specific instructions only when they solve a clear problem.

## Phase 3. Team workflow
- Standardize prompting, planning, verification, and review habits.
- Teach the team when to use `/plan`, `/review`, skills, and delegation.
revis- Use real frontend and backend tasks to reinforce the pattern.
