---
layout: none
---

<DeckFrame shell-class="subagents-shell">
  <SlideHeading
    title="Subagents"
    title-class="subagents-title"
    title-delay="0.10s"
  />
  <Subagents />
  <TenorGif postid="1461380403278441959" aspect-ratio="0.965863" />
</DeckFrame>

<style scoped>
.subagents-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 48px;
  align-items: start;
}

:deep(.subagents-title) {
  font-size: clamp(1.6rem, 2.2vw, 2.4rem);
  line-height: 1.04;
  letter-spacing: -0.05em;
  white-space: nowrap;
}
</style>

<!--
/fleet breaks your task into independent subtasks and runs them in parallel, each with its own agent and context window.

/delegate goes further — it runs in the cloud (this is github you know), runs async, commits to a new branch, and opens a draft PR.

Both are useful when the task is large and complex enough. 
But I don't recomend to use for every task. (this eats token so fast)
-->
