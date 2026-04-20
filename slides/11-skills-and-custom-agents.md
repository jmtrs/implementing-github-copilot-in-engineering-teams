---
layout: none
---

<DeckFrame shell-class="skills-shell">
  <SlideHeading
    title="Skills and custom agents"
    title-class="skills-title"
    title-delay="0.10s"
  />
  <SkillsAgents />
</DeckFrame>

<style scoped>
.skills-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 40px;
  align-items: start;
}

:deep(.skills-title) {
  font-size: clamp(1.6rem, 2.2vw, 2.4rem);
  line-height: 1.04;
  letter-spacing: -0.05em;
  white-space: nowrap;
}
</style>

<!--
Now Skills 

Skills are repeatable instruction packages. You define them once and invoke them by name.

Custom agents are specialized,they have their own tools, model configuration, and behavioral scope.

Both live in the repository, which means the team shares them.

Use them when a task is specialist enough to justify a dedicated pattern.
-->
