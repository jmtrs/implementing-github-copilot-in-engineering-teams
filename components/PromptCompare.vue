<template>
  <div class="prompt-compare">
    <div class="panel fade-up" style="animation-delay: 0.40s">
      <div class="panel-header">
        <span class="panel-mark bad-mark">✗</span>
        <h2 class="panel-title">Bad prompting</h2>
      </div>
      <ul class="panel-list">
        <li
          v-for="(item, i) in badItems"
          :key="item.label"
          class="panel-item"
          :style="{ opacity: 0, animation: `fadeUp 0.55s cubic-bezier(0.16,1,0.3,1) ${0.52 + i * 0.09}s forwards` }"
        >
          <span class="item-dot"></span>
          <span class="item-body">
            <span class="item-label">{{ item.label }}</span>
            <span class="item-example">{{ item.example }}</span>
          </span>
        </li>
      </ul>
    </div>

    <div class="divider fade-in" style="animation-delay: 0.38s"></div>

    <div class="panel fade-up" style="animation-delay: 0.58s">
      <div class="panel-header">
        <span class="panel-mark good-mark">✓</span>
        <h2 class="panel-title">Good prompting</h2>
      </div>
      <ul class="panel-list">
        <li
          v-for="(item, i) in goodItems"
          :key="item.label"
          class="panel-item"
          :style="{ opacity: 0, animation: `fadeUp 0.55s cubic-bezier(0.16,1,0.3,1) ${0.70 + i * 0.09}s forwards` }"
        >
          <span class="item-dot good-dot"></span>
          <span class="item-body">
            <span class="item-label">{{ item.label }}</span>
            <span class="item-example">{{ item.example }}</span>
          </span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
const badItems = [
  { label: 'Vague ask',            example: '"Fix the API"' },
  { label: 'Too much scope',       example: '"Rewrite the whole auth flow"' },
  { label: 'No success criteria',  example: 'No mention of what done looks like' },
  { label: 'No verification',      example: 'No test or check requested' },
  { label: 'No ownership boundary',example: 'Touches frontend and backend at once' },
]

const goodItems = [
  { label: 'Clear goal',           example: '"Add projectId validation to POST /projects"' },
  { label: 'Relevant context',     example: '"Route is in routes/projects.routes.js"' },
  { label: 'Constraints',          example: '"Do not change the response shape"' },
  { label: 'Expected output',      example: '"Return 400 if projectId is missing"' },
  { label: 'One small next step',  example: '"Only the validation — not the DB query"' },
]
</script>

<style scoped>
.prompt-compare {
  display: grid;
  grid-template-columns: 1fr 1px 1fr;
  gap: 0 36px;
  width: 100%;
  max-width: 980px;
  margin: 0 auto;
  align-items: start;
}

.divider {
  align-self: stretch;
  background: rgba(255, 255, 255, 0.08);
}

/* ── Panel ─────────────────────────────────────────────── */
.panel {
  padding: 24px 28px 26px;
  border-radius: 18px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

.panel-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 20px;
  padding-bottom: 16px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.07);
}

.panel-mark {
  font-family: var(--font-display);
  font-size: 1.2rem;
}

.good-mark {
  color: #40ff27;
}

.bad-mark {
  color: #ff4040;
}

.panel-title {
  margin: 0;
  font-family: var(--font-display);
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #8d8d8d;
}

/* ── List ──────────────────────────────────────────────── */
.panel-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 14px;
}

.panel-item {
  display: flex;
  align-items: flex-start;
  gap: 11px;
}

.item-dot {
  width: 5px;
  height: 5px;
  border-radius: 999px;
  background: #4a4a4a;
  flex-shrink: 0;
  margin-top: 0.55em;
}

.good-dot {
  background: #7a7a7a;
}

.item-body {
  display: flex;
  flex-direction: column;
  gap: 3px;
}

.item-label {
  font-family: var(--font-text);
  font-size: 0.9rem;
  line-height: 1.3;
  color: #c8c8c8;
}

.item-example {
  font-family: var(--font-code);
  font-size: 0.72rem;
  line-height: 1.35;
  color: #5e5e5e;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(10px); }
  to   { opacity: 1; transform: translateY(0); }
}
</style>
