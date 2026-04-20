<template>
  <div class="subagents">
    <div class="items">
      <div class="item fade-up" style="animation-delay: 0.34s">
        <code class="item-cmd">/fleet "..."</code>
        <p class="item-desc">parallel subtasks, each agent runs in its own isolated context</p>
      </div>
      <div class="item fade-up" style="animation-delay: 0.54s">
        <code class="item-cmd">/delegate "..."</code>
        <p class="item-desc">async cloud handoff, commits to a new branch, opens a draft PR</p>
      </div>
    </div>
    <p class="footer fade-up" style="animation-delay: 0.74s">Premium request cost scales with parallelism, use when the task justifies it.</p>
  </div>
</template>

<style scoped>
.subagents {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}

.items {
  display: flex;
  flex-direction: column;
  gap: 48px;
}

.item {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.item-cmd {
  font-family: var(--font-code);
  font-size: clamp(1.5rem, 3vw, 3rem);
  font-weight: 700;
  letter-spacing: -0.04em;
  color: #f5f5f5;
  line-height: 1;
}

.item-desc {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.92rem;
  line-height: 1.45;
  color: #8d8d8d;
}

.footer {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.78rem;
  color: rgba(141, 141, 141, 0.5);
  text-align: center;
}
</style>
