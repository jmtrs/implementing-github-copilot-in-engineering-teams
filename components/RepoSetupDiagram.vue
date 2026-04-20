<template>
  <div class="repo-diagram">
    <div class="workspace-row fade-up" style="animation-delay: 0.38s">
      <div class="workspace-anchor">
        <div class="workspace-node">
          <span class="workspace-label">parent workspace</span>
        </div>
        <span class="workspace-optional fade-in" style="animation-delay: 0.52s">* optional</span>
      </div>
    </div>


    <div class="connectors" aria-hidden="true">
      <svg class="connector-svg fade-in" style="animation-delay: 0.50s" viewBox="0 0 560 48" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
        <line x1="280" y1="0" x2="280" y2="24" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
        <line x1="280" y1="24" x2="100"  y2="24" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
        <line x1="280" y1="24" x2="460" y2="24" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
        <line x1="100"  y1="24" x2="100"  y2="48" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
        <line x1="460" y1="24" x2="460" y2="48" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
      </svg>
    </div>

    <div class="repos-row">
      <div class="repo-card card-surface fade-up" style="animation-delay: 0.58s">
        <div class="repo-header">
          <span class="repo-icon" aria-hidden="true"></span>
          <h2 class="repo-name">frontend</h2>
        </div>
        <ul class="file-list">
          <li class="file-entry primary fade-up" style="animation-delay: 0.82s">
            <span class="file-pill">.github/copilot-instructions.md</span>
            <span class="file-role">repository baseline</span>
          </li>
          <li class="file-entry secondary fade-up" style="animation-delay: 0.98s">
            <span class="file-pill muted">AGENTS.md</span>
            <span class="file-role">complementary</span>
          </li>
        </ul>
      </div>

      <div class="repo-card card-surface fade-up" style="animation-delay: 0.74s">
        <div class="repo-header">
          <span class="repo-icon" aria-hidden="true"></span>
          <h2 class="repo-name">backend</h2>
        </div>
        <ul class="file-list">
          <li class="file-entry primary fade-up" style="animation-delay: 0.98s">
            <span class="file-pill">.github/copilot-instructions.md</span>
            <span class="file-role">repository baseline</span>
          </li>
          <li class="file-entry secondary fade-up" style="animation-delay: 1.14s">
            <span class="file-pill muted">AGENTS.md</span>
            <span class="file-role">complementary</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.repo-diagram {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0;
  width: 100%;
  max-width: 860px;
  margin: 0 auto;
}

/* ── Workspace row ─────────────────────────────────────── */
.workspace-row {
  display: flex;
  justify-content: center;
}

.workspace-anchor {
  position: relative;
  display: inline-flex;
  align-items: center;
}

.workspace-node {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 10px 22px;
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.03);
}

.workspace-label {
  font-family: var(--font-code);
  font-size: 0.76rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #8d8d8d;
}

.workspace-optional {
  position: absolute;
  left: calc(100% + 14px);
  top: 50%;
  transform: translateY(-50%);
  white-space: nowrap;
  font-family: var(--font-text);
  font-size: 0.56rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #3a3a3a;
}

/* ── Connectors ────────────────────────────────────────── */
.connectors {
  width: 100%;
}

.connector-svg {
  display: block;
  width: 100%;
  height: 48px;
}

/* ── Repos row ─────────────────────────────────────────── */
.repos-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  width: 100%;
}

/* ── Repo card ─────────────────────────────────────────── */
.repo-card {
  padding: 24px 26px 22px;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.repo-header {
  display: flex;
  align-items: center;
  gap: 12px;
}

.repo-icon {
  display: block;
  width: 10px;
  height: 10px;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.25);
  flex-shrink: 0;
}

.repo-name {
  margin: 0;
  font-family: var(--font-display);
  font-size: 1.18rem;
  font-weight: 600;
  line-height: 1.1;
  letter-spacing: -0.03em;
  color: #f5f5f5;
}

/* ── File list ─────────────────────────────────────────── */
.file-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 10px;
}

.file-entry {
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.file-pill {
  display: inline-block;
  width: fit-content;
  padding: 5px 11px;
  border: 1px solid rgba(255, 255, 255, 0.11);
  border-radius: 999px;
  font-family: var(--font-code);
  font-size: 0.66rem;
  letter-spacing: 0.01em;
  color: #d7d7d7;
  background: rgba(255, 255, 255, 0.04);
}

.file-pill.muted {
  color: #8d8d8d;
  border-color: rgba(255, 255, 255, 0.06);
  background: transparent;
}

.file-role {
  padding-left: 12px;
  font-family: var(--font-text);
  font-size: 0.72rem;
  line-height: 1.2;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #5a5a5a;
}
</style>
