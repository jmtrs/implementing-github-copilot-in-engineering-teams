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
- `AGENTS.md` still exists as complementary guidance
- the audience already uses Copilot, but not always well
- the examples should be derived from a real project shape without naming the product

The structure includes:
- presentation title
- presentation goal
- 18-slide deck outline
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

# 18-slide presentation structure

---

## Slide 1. Why this needs a shared AI operating model

### Slide title
**Why this needs a shared AI operating model**

### Slide text
- AI is already part of development work.
- Many teams already use Copilot, but not always in the same way.
- Without one shared model, we get drift, review noise, and inconsistent results.

### Presenter notes
This slide should frame the talk around behavior, not tooling alone.

### Animation / Design
- Keep this slide simple.
- Use one title fade-up on entry.
- Reveal the bullets with a short staggered entrance.
- Do not add extra visual elements or complex motion.

Suggested speaking notes:

> AI is already part of development work. The question now is not access. The question is how we use it well as a team. If each person uses Copilot with a different approach, we get drift, review noise, and inconsistent quality. What we need is one shared way of working.

---

## Slide 2. How Copilot works in practice

### Slide title
**How Copilot works in practice**

### Slide text
- Copilot is not only autocomplete.
- It works through context, instructions, policies, and workflow.
- Enterprise, repository, and local usage all shape the result.

### Presenter notes
Keep this practical and not product-marketing.

### Animation / Design
- Use a split 50/50 layout.
- Put the visual on the left and the text on the right.
- The left side should use a real-looking coding image, not a diagram.
- Recommended visual: an editor with Copilot visibly completing or suggesting code inline.
- The image should feel real and legible at a glance, without too much small text.
- Avoid admin settings, dashboards, or configuration screens.
- Animate the image first with a soft fade-in.
- Then reveal the text on the right with a short staggered entrance.
- Keep the motion clean and restrained.

Suggested speaking notes:

> Copilot is not only autocomplete. In practice, it works through the context it sees, the instructions it receives, the policies that enable or disable features, and the workflow we expect people to follow. So rollout is not one switch. It is a stack of decisions.

---

## Slide 3. Three control layers

### Slide title
**Three control layers**

### Slide text
- Enterprise or organization
- Repository
- Local tool and user environment

### Presenter notes
This slide explains why rollout is never only an admin setting.

### Animation / Design
- Use a split 50/50 layout.
- Put the text on the left and the visual on the right.
- The right side should use a clear vertical diagram.
- Recommended visual: three stacked layers showing Enterprise or organization, Repository, and Local tool and user environment.
- The diagram should feel structured and easy to read, not decorative.
- Animate the diagram in sequence from top to bottom.
- Then reveal the text on the left with a short staggered entrance.
- Keep the motion restrained and clean.

Suggested speaking notes:

> We need to separate three layers. Enterprise or organization controls access and policy. The repository controls shared working rules. The local tool and user environment still matter, especially when people use terminals, agents, or other AI tools outside one standard path.

---

## Slide 4. What Enterprise and the organization control

### Slide title
**What Enterprise and the organization control**

### Slide text
- Access, features, policies, and model choices
- GitHub-based review and agent capabilities
- Metrics and visibility, with uneven coverage by surface

### Presenter notes
This compresses the governance story into one slide.

Suggested speaking notes:

> At enterprise and organization level, we can decide who gets access, which features are enabled, which models are available, and whether some GitHub-based agent capabilities are allowed. We can also review usage data, but we should be careful because metrics do not cover every Copilot surface in the same way.

---

## Slide 5. What Enterprise does not solve

### Slide title
**What Enterprise does not solve**

### Slide text
- Repository architecture
- Frontend and backend contracts
- Prompt quality and task scoping
- Verification expectations for real changes

### Presenter notes
This slide prevents an admin-only interpretation.

Suggested speaking notes:

> Enterprise gives us policy and control, but it does not solve repository-level engineering questions. It does not know our contracts, our ownership model, our preferred task size, or what counts as enough verification. Those things still belong to the repositories and to the team workflow.

---

## Slide 6. What a real repo setup looks like

### Slide title
**What a real repo setup looks like**

### Slide text
- Two real repositories coordinated from one parent workspace
- Repository-wide Copilot baseline already configured
- `AGENTS.md` still useful as complementary guidance

### Presenter notes
This is where the case study becomes concrete.

Suggested speaking notes:

> In our case, the right mental model is not one physical monorepo. It is one working workspace with a frontend repository and a backend repository. The Copilot baseline lives in the real repositories where the code and Git history live. Repository-wide `copilot-instructions.md` gives the most portable Copilot baseline, and `AGENTS.md` still helps, especially for agent workflows.

---

## Slide 7. The baseline we assume is already mounted

### Slide title
**The baseline we assume is already mounted**

### Slide text
- `/.github/copilot-instructions.md` in each real repository
- `AGENTS.md` as complementary guidance
- Path-specific rules only where they add real value

### Presenter notes
This slide should make the setup feel already solved.

Suggested speaking notes:

> We are not spending this talk on bootstrap. We assume the minimum baseline is already mounted. In practice, that means repository-wide Copilot instructions in each real repo, plus `AGENTS.md` as complementary guidance. Path-specific instructions are optional and should only appear where they solve a real problem.

---

## Slide 8. What each repository still must define

### Slide title
**What each repository still must define**

### Slide text
- Shared rules for the code it owns
- Contract ownership with the other side
- Real verification commands and quality expectations

### Presenter notes
Keep this centered on engineering reality.

Suggested speaking notes:

> Even with Enterprise in place, each repository still needs to define the rules that matter in that codebase. That includes its architecture, how contracts are owned, and how changes are validated. This is where Copilot becomes project-aware instead of generic.

---

## Slide 9. What good prompting looks like

### Slide title
**What good prompting looks like**

### Slide text
- Clear goal
- Relevant context
- Constraints and limits
- Expected output
- One small next step

### Presenter notes
This is the first slide of the practical block.

Suggested speaking notes:

> Good prompting is not about sounding clever. It is about giving Copilot the right shape of task. A good prompt says what the goal is, what context matters, what constraints apply, what kind of output we want, and what the next step should be. The smaller and clearer the first step, the better the result.

---

## Slide 10. What bad prompting looks like

### Slide title
**What bad prompting looks like**

### Slide text
- Vague asks
- Too much scope in one prompt
- No success criteria
- No verification request
- No ownership boundaries

### Presenter notes
This slide should feel uncomfortably familiar.

Suggested speaking notes:

> Most bad results start with bad prompting. The usual pattern is a vague request, too much scope, no clear success criteria, no validation step, and no ownership boundary. Then people blame the tool, even though the task itself was underspecified.

---

## Slide 11. The CLI patterns and capabilities that matter daily

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

## Slide 12. How to use `/plan` well

### Slide title
**How to use `/plan` well**

### Slide text
- Use it for complex or risky work
- Let Copilot inspect before coding
- Review the plan
- Execute one small step first

### Presenter notes
This is one of the key habit-change slides.

Suggested speaking notes:

> `/plan` is one of the highest leverage habits. Use it when the task is complex, risky, or cross-layer. Let Copilot inspect the codebase first. Review the plan. Then execute only one small step. That keeps context clean and makes the work reviewable.

---

## Slide 13. How to use review and verification well

### Slide title
**How to use review and verification well**

### Slide text
- Ask for review before merge
- Verify the relevant files and commands
- Ask for limits, risks, and gaps
- Iterate in small steps

### Presenter notes
This should reinforce engineering discipline.

Suggested speaking notes:

> Copilot should not be the last reviewer of its own work. Ask for review, ask what was verified, ask what still looks risky, and keep the loop small. The point is not speed alone. The point is controlled speed.

---

## Slide 14. Skills, custom agents, and subagents

### Slide title
**Skills, custom agents, and subagents**

### Slide text
- Skills for repeatable specialist tasks
- Custom agents for specialized roles
- Subagents for delegation and parallel work
- Use them when complexity justifies them

### Presenter notes
Keep this concrete and anti-hype.

Suggested speaking notes:

> Skills help with repeatable specialist tasks. Custom agents let Copilot use more specialized roles. Subagents help delegate and parallelize parts of the work. These are useful when complexity justifies them. They are not things we need to force into every task.

---

## Slide 15. What quality and safety mean here

### Slide title
**What quality and safety mean here**

### Slide text
- Keep routes thin
- Use parameterized SQL only
- Use `projectId`, not `scopeId`
- Keep frontend and backend contracts aligned

### Presenter notes
This slide lands better after the CLI block.

Suggested speaking notes:

> After we teach the workflow, we can make the guardrails concrete. In this case, thin routes matter. Parameterized SQL matters. The payload convention matters. Contract alignment matters. These are not generic AI rules. These are the rules that keep this workspace safe and maintainable.

---

## Slide 16. What changes if other AI tools are also allowed

### Slide title
**What changes if other AI tools are also allowed**

### Slide text
- The repo can share some rules across tools
- GitHub-governed third-party agents are not the same as local AI tools
- Each extra tool adds another config and permission model
- More tools mean more rollout work and more drift risk

### Presenter notes
Keep this near the end so it does not break the practical block.

Suggested speaking notes:

> Allowing more than one AI tool is possible. The repositories can still provide shared rules. But we should separate two cases. One case is third-party agents enabled inside GitHub governance. The other case is local tools that have their own configuration and permissions outside that path. In both cases the governance burden becomes higher.

---

## Slide 17. Demo 1. From bad prompt to good prompt

### Slide title
**Demo 1: from bad prompt to good prompt**

### Slide text
- Show a vague prompt
- Improve it with context and constraints
- Use `/plan`
- Execute only the first step

### Presenter notes
This demo should prove why prompt quality changes the outcome.

Suggested speaking notes:

> This demo is about behavior, not features. We start with a weak prompt, improve it, ask for a plan, and keep the work to one small step. The audience should see that most day-to-day gains come from better prompting and better scoping.

---

## Slide 18. Demo 2 and next steps

### Slide title
**Demo 2 and next steps**

### Slide text
- Use one small cross-layer task
- Review ownership and contract impact
- Verify before closing
- End with explicit team next steps

### Presenter notes
This is the end-to-end workflow demo and the explicit close.

Suggested speaking notes:

> The second demo should show one realistic task across repository boundaries. We check ownership, keep the step small, verify the result, and close with the next team steps we want to standardize. That is the operating model we want people to remember.

---

# Demo section

## Demo 1. From bad prompt to good prompt

### Goal
Show that prompt quality and task framing directly change the usefulness of Copilot CLI.

### What should already be true before the demo
- The frontend repository already has its repository-wide Copilot baseline.
- The backend repository already has its repository-wide Copilot baseline.
- Both repositories use `/.github/copilot-instructions.md` as the main Copilot baseline.
- `AGENTS.md` remains available as complementary guidance.

### Suggested flow
1. Start with a vague prompt that asks for too much.
2. Show why the result is weak or underspecified.
3. Rewrite the prompt with:
   - clear goal
   - relevant context
   - constraints
   - expected output
   - one small next step
4. Run `/plan`.
5. Continue with the first step only.

### Example bad prompt

```text
Fix the API and frontend for this feature.
```

### Example improved prompt

```text
/plan Update one API payload field used by a frontend service wrapper.
Check the owning backend route and model first.
Then identify the frontend wrapper that must stay aligned.
Do not implement the whole change at once.
Propose the first small step only.
```

### What to explain after the demo
- Bad output often starts with bad prompting.
- `/plan` is useful when scope or risk is unclear.
- Smaller first steps improve both quality and reviewability.

---

## Demo 2. One real workflow end to end

### Goal
Show the daily operating model for a small cross-layer task.

### Suggested flow
1. Start from repository rules, not from a blank prompt.
2. Identify the owning backend and frontend files.
3. Ask for one small implementation step.
4. Ask for verification or `/review`.
5. Summarize remaining risks or gaps.

### Suggested CLI prompt

```text
/plan Update one API payload field used by a frontend service wrapper.
Check the owning backend route and model first.
Then identify the frontend wrapper that must stay aligned.
```

Then continue with:

```text
Implement one small step only.
After that, run the relevant verification and explain any remaining risk.
```

### What to explain after the demo
- We start from repository rules.
- We check ownership and contract impact first.
- We keep the task small.
- We verify before closing.
- This is the repeatable pattern the team should adopt.

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
- `AGENTS.md` is still useful, especially for agent workflows, but it should not replace the repository-wide Copilot baseline in the presentation.
- Support is not identical across all Copilot surfaces. The safest baseline to present first is `.github/copilot-instructions.md` inside each real repository.

---

# Copilot CLI usage notes

## What good prompting looks like

Good prompts usually include:
- a clear goal
- relevant context
- constraints
- expected output
- one small next step

## What bad prompting looks like

Bad prompts usually fail because they:
- are vague
- ask for too much in one step
- omit verification
- omit ownership boundaries
- do not define success

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

## Phase 4. Adoption review
- Review whether Enterprise policy, repository baseline, and team workflow are aligned.
- Expand only where repeated problems appear.
- Reassess mixed-tool use only after the Copilot baseline is stable.
