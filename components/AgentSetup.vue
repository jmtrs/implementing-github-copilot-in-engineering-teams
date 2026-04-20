<template>
  <div class="agent-setup fade-up" style="animation-delay: 0.50s">
    <div class="agent-item">
      <code class="agent-path">.github/agents/test-writer.agent.md</code>
      <span class="agent-desc">writes Jest + Supertest tests for a route</span>
    </div>
    <div class="agent-item">
      <code class="agent-path">.github/agents/sql-reviewer.agent.md</code>
      <span class="agent-desc">reviews SQL in model files for injection risks</span>
    </div>
  </div>
</template>

<style scoped>
.agent-setup {
  display: flex;
  flex-direction: column;
  gap: 28px;
}

.agent-item {
  display: flex;
  flex-direction: column;
  gap: 6px;
  padding-left: 16px;
  border-left: 1px solid rgba(255, 255, 255, 0.09);
}

.agent-path {
  font-family: var(--font-code);
  font-size: 0.88rem;
  letter-spacing: -0.01em;
  color: #f5f5f5;
}

.agent-desc {
  font-family: var(--font-text);
  font-size: 0.82rem;
  color: #8d8d8d;
}
</style>
