---
layout: none
---

<DeckFrame shell-class="cli-shell">
  <div class="cli-header">
    <SlideHeading
      kicker="Copilot CLI"
      title="The Copilot CLI patterns"
      title-class="cli-title"
      kicker-delay="0.10s"
      title-delay="0.24s"
    />
  </div>

  <ul class="cli-list">
    <li class="cli-item fade-up" style="animation-delay: 0.50s">
      <code class="cli-cmd">conversation</code>
      <span class="cli-desc">scoped questions, fast context, no task switch</span>
    </li>
    <li class="cli-item fade-up" style="animation-delay: 0.64s">
      <code class="cli-cmd">/plan</code>
      <span class="cli-desc">let Copilot inspect before coding, for complex or risky work</span>
    </li>
    <li class="cli-item fade-up" style="animation-delay: 0.78s">
      <code class="cli-cmd">/review</code>
      <span class="cli-desc">ask for gaps, risks, and what was not verified</span>
    </li>
    <li class="cli-item fade-up" style="animation-delay: 0.92s">
      <code class="cli-cmd">skills</code>
      <span class="cli-desc">repeatable specialist tasks without rewriting the prompt</span>
    </li>
    <li class="cli-item fade-up" style="animation-delay: 1.06s">
      <code class="cli-cmd">agents / subagents</code>
      <span class="cli-desc">specialized roles and parallel delegation when complexity justifies it</span>
    </li>
  </ul>
</DeckFrame>

<style scoped>
.cli-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 44px;
  align-items: start;
}

.cli-header {
  padding-top: 4px;
}

:deep(.cli-title) {
  font-size: clamp(2rem, 2.8vw, 3rem);
  line-height: 1.04;
  letter-spacing: -0.05em;
  max-width: 16ch;
}

.cli-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 0;
}

.cli-item {
  display: grid;
  grid-template-columns: 200px 1fr;
  align-items: baseline;
  gap: 24px;
  padding: 16px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}

.cli-item:last-child {
  border-bottom: none;
}

.cli-cmd {
  font-family: var(--font-code);
  font-size: 0.96rem;
  letter-spacing: -0.01em;
  color: #f5f5f5;
}

.cli-desc {
  font-family: var(--font-text);
  font-size: 0.92rem;
  line-height: 1.45;
  color: #8d8d8d;
}
</style>

<!--
Copilot CLI patterns.

We need to know a few patterns to help us work better with Copilot.

Normal conversation for scoped questions. 

/plan before complex or risky work. 

/review to catch what Copilot missed. 

Skills for repeatable tasks. 

And agents when the problem is big enough to delegate.

Let's take a look to some of these patterns.
-->
