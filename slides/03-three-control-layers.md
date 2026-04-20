---
layout: none
---

<DeckFrame shell-class="layers-shell">
  <div class="layers-header">
    <SlideHeading
      kicker="Layered model"
      title="Three control layers"
      title-class="layers-title"
      kicker-delay="0.08s"
      title-delay="0.2s"
    />
    <p class="layers-intro fade-up" style="animation-delay:0.56s">
      Rollout only works when these three layers reinforce each other.
    </p>
  </div>
  <LayerBands />
</DeckFrame>

<style scoped>
.layers-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 56px;
}
.layers-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding-top: 18px;
}
:deep(.layers-title) {
  max-width: none;
  white-space: nowrap;
  font-size: clamp(2.55rem, 3.35vw, 3.25rem);
  line-height: 1;
  letter-spacing: -0.04em;
}
.layers-intro {
  margin: 22px 0 0;
  max-width: 42rem;
  font-size: 1rem;
  line-height: 1.55;
  color: #9a9a9a;
}
</style>

<!--
This slide breaks the rollout into three control layers.

At the organization layer, we define policy and access.

At the repository layer, we define the shared rules for engineering work.

And at the local tool and user environment layer, execution context shapes how people actually use Copilot day to day.

That is why these layers need to work together.
-->
