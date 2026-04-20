<template>
  <div class="compare">
    <div class="panel panel--dim fade-up" style="animation-delay: 0.36s">
      <p class="panel-label">Direct prompt</p>
      <code class="panel-cmd panel-cmd--dim">"Add a loading state to the login button"</code>
      <ul class="panel-list">
        <li>Copilot infers from the open file</li>
        <li>No codebase inspection</li>
        <li>May miss existing patterns</li>
      </ul>
    </div>

    <div class="panel panel--bright fade-up" style="animation-delay: 0.54s">
      <p class="panel-label panel-label--bright">/plan</p>
      <code class="panel-cmd">/plan "Add a loading state to the login button"</code>
      <ul class="panel-list panel-list--bright">
        <li>Inspects auth hook, button component, existing patterns</li>
        <li>Asks clarifying questions before writing</li>
        <li>Generates a plan — review, approve, execute one step</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.compare {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.panel {
  padding: 22px 24px 24px;
  border-radius: 14px;
  border: 1px solid rgba(255, 255, 255, 0.07);
  display: grid;
  gap: 12px;
  align-content: start;
}

.panel--dim {
  background: rgba(255, 255, 255, 0.02);
}

.panel--bright {
  background: rgba(255, 255, 255, 0.04);
  border-color: rgba(255, 255, 255, 0.12);
}

.panel-label {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #606060;
}

.panel-label--bright {
  color: #8d8d8d;
}

.panel-cmd {
  margin: 0;
  font-family: var(--font-code);
  font-size: 0.84rem;
  letter-spacing: -0.01em;
  color: #f5f5f5;
  line-height: 1.4;
}

.panel-cmd--dim {
  color: #606060;
}

.panel-list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: grid;
  gap: 8px;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  padding-top: 12px;
}

.panel-list li {
  font-family: var(--font-text);
  font-size: 0.84rem;
  line-height: 1.45;
  color: #606060;
  padding-left: 12px;
  position: relative;
}

.panel-list li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.58em;
  width: 4px;
  height: 4px;
  border-radius: 999px;
  background: #606060;
}

.panel-list--bright li {
  color: #8d8d8d;
}

.panel-list--bright li::before {
  background: #5e5e5e;
}
</style>
