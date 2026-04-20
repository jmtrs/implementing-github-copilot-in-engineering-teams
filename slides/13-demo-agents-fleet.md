---
layout: none
---

<DeckFrame shell-class="demo2-shell">
  <SlideHeading
    kicker="Live demo 02"
    title="Agents and fleet"
    title-class="demo2-title"
    kicker-delay="0.10s"
    title-delay="0.24s"
  />
  <AgentSetup />
  <p class="lets-fleet fade-up" style="animation-delay: 0.72s">Let's fleet them.</p>
</DeckFrame>

<style scoped>
.demo2-shell {
  display: grid;
  grid-template-rows: auto auto 1fr;
  gap: 36px;
  align-items: start;
}

:deep(.demo2-title) {
  font-size: clamp(2rem, 2.8vw, 3rem);
  line-height: 1.04;
  letter-spacing: -0.05em;
  white-space: nowrap;
}

.lets-fleet {
  margin: 0;
  align-self: end;
  font-family: var(--font-display);
  font-size: clamp(2rem, 4vw, 4.5rem);
  font-weight: 700;
  letter-spacing: -0.05em;
  color: #f5f5f5;
  line-height: 1;
}
</style>

<!--
We have two agents already in the repo. One writes integration tests. The other reviews SQL for injection risks.

Both are markdown files in .github/agents

Now we run /fleet and delegate both tasks at the same time. Each agent runs in its own context. No one blocks the other.
-->
