<template>
  <div class="skills-agents">
    <div class="split-grid">
      <div class="block fade-up" style="animation-delay: 0.30s">
        <span class="block-label">skills</span>
        <ul class="cmd-list">
          <li class="cmd-item">
            <code class="cmd">/skills list</code>
            <span class="cmd-desc">see what is available</span>
          </li>
          <li class="cmd-item">
            <code class="cmd">/generate-tests "..."</code>
            <span class="cmd-desc">invoke by name</span>
          </li>
        </ul>
        <p class="block-desc">repeatable instruction packages, define once, invoke anywhere</p>
        <p class="block-location">.github/skills/SKILL.md</p>
      </div>

      <div class="v-divider"></div>

      <div class="block fade-up" style="animation-delay: 0.46s">
        <span class="block-label">agents</span>
        <ul class="cmd-list">
          <li class="cmd-item">
            <code class="cmd">/agent "..."</code>
            <span class="cmd-desc">open the agent selector</span>
          </li>
          <li class="cmd-item">
            <code class="cmd">Use the security-auditor agent to check ...</code>
            <span class="cmd-desc">explicit invocation</span>
          </li>
        </ul>
        <p class="block-desc">own tools, model, and behavioral scope</p>
        <p class="block-location">.github/agents/&lt;name&gt;.agent.md</p>
      </div>
    </div>

    <p class="footer fade-up" style="animation-delay: 0.62s">Both live in the repository, the team shares them.</p>
  </div>
</template>

<style scoped>
.skills-agents {
  display: flex;
  flex-direction: column;
  gap: 28px;
}

.split-grid {
  display: grid;
  grid-template-columns: 1fr 1px 1fr;
  gap: 0 40px;
  align-items: start;
}

.v-divider {
  align-self: stretch;
  background: rgba(255, 255, 255, 0.09);
}

.block {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.block-label {
  font-family: var(--font-code);
  font-size: 0.78rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #8d8d8d;
}

.cmd-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 0;
}

.cmd-item {
  display: grid;
  grid-template-columns: 1fr;
  gap: 4px;
  padding: 14px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}

.cmd-item:first-child {
  border-top: 1px solid rgba(255, 255, 255, 0.06);
}

.cmd {
  font-family: var(--font-code);
  font-size: 0.90rem;
  letter-spacing: -0.01em;
  color: #f5f5f5;
}

.cmd-desc {
  font-family: var(--font-text);
  font-size: 0.82rem;
  line-height: 1.45;
  color: #8d8d8d;
}

.block-desc {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.88rem;
  line-height: 1.5;
  color: #8d8d8d;
}

.block-location {
  margin: 0;
  font-family: var(--font-code);
  font-size: 0.78rem;
  letter-spacing: 0.01em;
  color: rgba(141, 141, 141, 0.6);
}

.footer {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.88rem;
  color: #8d8d8d;
  border-top: 1px solid rgba(255, 255, 255, 0.06);
  padding-top: 20px;
}
</style>
