---
layout: none
---

<DeckFrame shell-class="control-shell">
  <div class="control-header">
    <SlideHeading
      kicker=""
      title="What Enterprise and the organization control"
      title-class="control-title"
      title-delay="0.18s"
    />
  </div>
  <ControlMap />
  <p class="control-note fade-in" style="animation-delay:1.46s">set centrally or delegated to organization owners</p>
</DeckFrame>

<style scoped>
.control-shell {
  display: grid;
  grid-template-rows: auto 1fr auto;
  gap: 6px;
}
.control-header {
  display: flex;
  justify-content: center;
  text-align: center;
  padding-top: 0;
}
:deep(.control-title) {
  max-width: 22ch;
  font-size: clamp(1.42rem, 1.72vw, 1.82rem);
  line-height: 1.08;
  letter-spacing: -0.045em;
}
.control-note {
  margin: -4px 0 0;
  text-align: center;
  font-size: 0.74rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #8d8d8d;
}
</style>

<!--
At enterprise and organization level, GitHub gives us a real control surface.

We can manage access, define policies, control model availability, and decide which GitHub-native AI capabilities are allowed.

In GitHub Docs, this lives under AI controls, including Policies, Models, Agents, MCP, and metrics.

For example, enterprise owners can define policies centrally or delegate them to organization owners.

Policies are grouped into feature, privacy, and models.

Cloud agent and MCP are controlled in the AI controls area, and usage visibility comes from dashboards and APIs.

That visibility is useful, but it is not complete across every surface.

So this layer matters, but it defines the operating envelope more than the day-to-day engineering workflow.
-->
