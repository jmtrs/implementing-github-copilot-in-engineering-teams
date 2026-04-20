---
layout: none
---

<DeckFrame shell-class="demo-shell">
  <SlideHeading
    kicker="Live demo 01"
    title="Add a loading state to the login button"
    title-class="demo-title"
    kicker-delay="0.10s"
    title-delay="0.22s"
  />
  <DemoCompare />
  <p class="lets-try fade-up" style="animation-delay: 0.80s">Let's try it.</p>
</DeckFrame>

<style scoped>
.demo-shell {
  display: grid;
  grid-template-rows: auto 1fr auto;
  gap: 32px;
  align-items: start;
}

.lets-try {
  margin: 0;
  font-family: var(--font-display);
  font-size: clamp(2rem, 4vw, 4.5rem);
  font-weight: 700;
  letter-spacing: -0.05em;
  color: #f5f5f5;
  line-height: 1;
}

:deep(.demo-title) {
  font-size: clamp(1.4rem, 2vw, 2.1rem);
  letter-spacing: -0.04em;
  line-height: 1.1;
  max-width: none;
}
</style>

<!--
We are going to run this demo live.

The scenario is a login button with no visual feedback — the user clicks and nothing happens until the response comes back.

We will run the same task twice: first with a direct prompt, then with /plan.

With /plan, we also tell Copilot to ask if it has doubts before implementing -that is the Socratic mode.

Let's see how this works.
-->
