---
layout: none
---

<div class="slide-base">
  <div class="closing-center">
    <p class="closing-main anim-hidden">Thank you.</p>
    <p class="closing-question anim-hidden">Any questions?<span class="cursor"></span></p>
  </div>
  <p class="closing-credit anim-hidden">Desde la Vega Baja con ❤️ José Miguel Torres Hernández</p>
</div>

<style scoped>
.closing-center {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
  text-align: center;
}

.closing-question {
  margin: 0;
  font-family: var(--font-text);
  font-size: 1.2rem;
  letter-spacing: -0.02em;
  color: #8d8d8d;
  animation: fadeUp 0.75s cubic-bezier(0.16, 1, 0.3, 1) 0.9s forwards;
}

.cursor {
  display: inline-block;
  width: 10px;
  height: 1em;
  margin-left: 6px;
  vertical-align: -0.12em;
  background: #8d8d8d;
  animation: blink 1s step-end infinite;
}

.closing-main {
  margin: 0;
  font-family: var(--font-display);
  font-size: clamp(3rem, 6vw, 6.5rem);
  font-weight: 700;
  letter-spacing: -0.06em;
  line-height: 1;
  color: #f5f5f5;
  animation: fadeUp 0.9s cubic-bezier(0.16, 1, 0.3, 1) 0.2s forwards;
}

.closing-credit {
  position: absolute;
  bottom: 36px;
  right: 48px;
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.72rem;
  letter-spacing: -0.01em;
  color: #8d8d8d;
  opacity: 0;
  animation: fadeIn 0.5s ease 1.8s forwards;
}

@keyframes blink {
  0%, 49% { opacity: 0.95; }
  50%, 100% { opacity: 0.15; }
}
</style>

<!--
And thats all.

Thank you for your attention. 

Any questions?
-->
