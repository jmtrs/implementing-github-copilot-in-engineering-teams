---
layout: none
---

<DeckFrame grid split shell-class="repo-rules-shell">
  <div class="repo-rules-left">
    <SlideHeading
      kicker="Repository layer"
      title="What each repository must define"
      title-class="repo-rules-title"
      kicker-delay="0.10s"
      title-delay="0.24s"
    />
  </div>

  <ul class="repo-rules-list">
    <li class="rule-item fade-up" style="animation-delay: 0.54s">
      <h3 class="rule-label">Shared rules for the code it owns</h3>
      <p class="rule-desc">tech stack, architecture, coding guidelines with reasoning</p>
      <code class="rule-pill">.github/copilot-instructions.md</code>
    </li>
    <li class="rule-item fade-up" style="animation-delay: 0.76s">
      <h3 class="rule-label">Contract ownership with the other side</h3>
      <p class="rule-desc">path-specific rules with <span class="inline-code">applyTo</span> glob patterns per area</p>
      <code class="rule-pill">.github/instructions/*.instructions.md</code>
    </li>
    <li class="rule-item fade-up" style="animation-delay: 0.98s">
      <h3 class="rule-label">Real verification commands</h3>
      <p class="rule-desc">commands in the file, not just tool names</p>
      <code class="rule-pill">npm test · pytest -v · npm run build</code>
    </li>
  </ul>
</DeckFrame>

<style scoped>
:deep(.repo-rules-shell) {
  align-items: center;
}

.repo-rules-left {
  padding-right: 24px;
}

:deep(.repo-rules-title) {
  font-size: clamp(1.7rem, 2.2vw, 2.4rem);
  line-height: 1.06;
  letter-spacing: -0.045em;
  max-width: 14ch;
}

.repo-rules-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 28px;
}

.rule-item {
  display: grid;
  gap: 6px;
}

.rule-label {
  margin: 0;
  font-family: var(--font-display);
  font-size: 0.98rem;
  font-weight: 600;
  line-height: 1.2;
  letter-spacing: -0.025em;
  color: #f5f5f5;
}

.rule-desc {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.84rem;
  line-height: 1.45;
  color: #8d8d8d;
}

.inline-code {
  font-family: var(--font-code);
  font-size: 0.78rem;
  color: #c0c0c0;
}

.rule-pill {
  display: inline-block;
  margin-top: 4px;
  padding: 4px 11px;
  border: 1px solid rgba(255, 255, 255, 0.09);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.04);
  font-family: var(--font-code);
  font-size: 0.66rem;
  letter-spacing: 0.01em;
  color: #b0b0b0;
}
</style>

<!--
Even with Enterprise in place, each repository needs to define the rules that matter in that codebase.

That includes its architecture, how contracts are owned, and how changes are validated.

Path-specific instructions let each side of the workspace define its own rules without duplication.

And verification commands must be real commands in the file, not just tool names.

This is where Copilot becomes project-aware instead of generic.
-->
