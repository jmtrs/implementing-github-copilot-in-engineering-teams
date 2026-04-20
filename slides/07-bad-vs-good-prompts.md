---
layout: none
---

<DeckFrame shell-class="compare-shell">
  <div class="compare-header">
    <SlideHeading
      title="Bad prompts vs good prompts"
      title-class="compare-title"
      title-delay="0.18s"
    />
  </div>
  <PromptCompare />
</DeckFrame>

<style scoped>
.compare-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 28px;
  align-items: start;
}
.compare-header {
  display: flex;
  justify-content: center;
  text-align: center;
}
:deep(.compare-title) {
  font-size: clamp(1.4rem, 1.85vw, 2rem);
  line-height: 1.06;
  letter-spacing: -0.04em;
  white-space: nowrap;
  max-width: none;
}
</style>

<!--
On the left is the pattern that usually produces weak results.

The ask is vague, the scope is too large, there is no clear success criteria, no verification step, and no ownership boundary.

On the right is the same task shaped properly.

The goal is clear, the relevant context is included, constraints are explicit, the expected output is defined, and the next step is small enough to execute well.

The point is simple: the tool usually reflects the shape of the task we give it.
-->
