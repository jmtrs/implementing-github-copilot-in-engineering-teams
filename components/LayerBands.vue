<template>
  <div class="layers-visual">
    <div class="layer-band fade-up" style="animation-delay: 0.42s">
      <div class="band-copy">
        <h2>Enterprise / organization</h2>
        <p>policy and access</p>
        <code>AI controls -> Copilot -> CLI</code>
      </div>
    </div>
    <div class="layer-band fade-up" style="animation-delay: 0.66s">
      <div class="band-copy">
        <h2>Repository</h2>
        <p>shared rules</p>
        <code>.github/copilot-instructions.md</code>
      </div>
    </div>
    <div class="layer-band fade-up" style="animation-delay: 0.9s">
      <div class="band-copy">
        <h2>Local tool and user environment</h2>
        <p>execution context</p>
        <code>$HOME/.copilot/copilot-instructions.md</code>
      </div>
    </div>
  </div>
</template>

<style scoped>
.layers-visual {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 24px;
  align-items: stretch;
  width: min(1260px, 100%);
  margin: 0 auto;
}
.layer-band {
  min-height: 138px;
  padding: 18px 20px 16px;
  border-radius: 26px;
  border: 1px solid rgba(255,255,255,0.09);
  background: rgba(255,255,255,0.01);
  box-shadow: none;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
.band-copy h2 {
  margin: 0;
  font-family: var(--font-display);
  font-size: 1.18rem;
  line-height: 1.1;
  letter-spacing: -0.03em;
  color: #f5f5f5;
}
.band-copy p {
  margin: 10px 0 0;
  font-family: var(--font-text);
  color: #8d8d8d;
  font-size: 0.92rem;
  line-height: 1.12;
}
.band-copy code {
  display: block;
  margin-top: 13px;
  padding: 0;
  border: 0;
  background: transparent;
  font-family: var(--font-text);
  font-size: 0.76rem;
  line-height: 1.28;
  color: #d7d7d7;
  white-space: normal;
  overflow-wrap: anywhere;
}
</style>
