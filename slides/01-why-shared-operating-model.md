---
layout: none
---

<DeckFrame micro="operating model · workflow · quality" shell-class="why-shell">
  <div class="why-layout">
    <div class="why-left">
      <SlideHeading
        kicker="Shared way of working"
        title="Why this needs a shared AI operating model"
        title-class="why-title"
        kicker-delay="0.08s"
        title-delay="0.2s"
      />
    </div>
    <div class="why-right">
      <p class="why-intro fade-up" style="animation-delay:0.54s">The problem is not access. The problem is using Copilot with one shared standard.</p>
      <BulletStack
        class-name="why-bullets"
        :items="[
          'AI is already part of development work.',
          'Many teams already use Copilot, but not always in the same way.',
          'Without one shared model, AI adoption creates drift, review noise, and uneven quality.'
        ]"
        :start-delay="0.82"
        :step="0.22"
      />
    </div>
  </div>
</DeckFrame>

<style scoped>
.why-shell {
  display: flex;
  align-items: center;
}
.why-layout {
  position: relative;
  z-index: 1;
  width: 100%;
  display: grid;
  grid-template-columns: minmax(0, 1.15fr) minmax(360px, 0.85fr);
  gap: 48px;
  align-items: end;
}
.why-left {
  max-width: 760px;
}
.why-right {
  padding-bottom: 18px;
}
.why-title {
  max-width: 9.5ch;
  font-size: clamp(3.25rem, 5.15vw, 4.35rem);
  line-height: 0.98;
}
.why-intro {
  margin: 0 0 18px;
  max-width: 24rem;
  font-size: 1.02rem;
  line-height: 1.5;
  color: #9a9a9a;
}
:deep(.why-bullets) {
  margin-top: 0;
  gap: 18px;
}
:deep(.why-bullets .bullet-row) {
  font-size: 1rem;
  line-height: 1.52;
}
:deep(.why-bullets .bullet-dot) {
  margin-top: 0.64em;
}
</style>

<!--
AI is already part of development work.

The question now is not access.

The question is how we use it well as a team.

If each person uses Copilot with a different approach, we get drift, review noise, and uneven quality.

What we need is one shared way of working.
-->
