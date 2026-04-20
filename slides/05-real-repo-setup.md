---
layout: none
---

<DeckFrame shell-class="repo-setup-shell">
  <div class="repo-setup-header">
    <SlideHeading
      title="What an AI repo setup looks like"
      title-class="repo-setup-title"
      title-delay="0.18s"
    />
  </div>
  <RepoSetupDiagram />
</DeckFrame>

<style scoped>
.repo-setup-shell {
  display: grid;
  grid-template-rows: auto 1fr;
  gap: 28px;
}
.repo-setup-header {
  display: flex;
  justify-content: center;
  text-align: center;
  padding-top: 0;
}
:deep(.repo-setup-title) {
  font-size: clamp(1.8rem, 2.4vw, 2.55rem);
  line-height: 1.06;
  letter-spacing: -0.045em;
  max-width: 18ch;
}
</style>

<!--
Let's talk about them.

In our case, our working workspace has a frontend repository and a backend repository.

Copilot lives in the repositories because that's where the code is.

Repository-wide copilot-instructions.md gives us the most portable Copilot configuration, and AGENTS.md helps, especially for agent workflows.
-->
