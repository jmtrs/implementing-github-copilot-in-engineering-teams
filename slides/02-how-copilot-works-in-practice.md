---
layout: none
---

<DeckFrame
  micro=""
  grid
  split
>
  <EditorWorkflowCard />
  <div>
    <SlideHeading
      kicker="Practical model"
      title="How Copilot works in practice"
      kicker-delay="0.42s"
      title-delay="0.56s"
    />
    <BulletStack
      :items="[
        'Copilot is not only autocomplete.',
        'It works through context, instructions, policies, and workflow.',
        'The result depends on the environment we create around it.'
      ]"
      :start-delay="0.86"
      :step="0.22"
    />
  </div>
</DeckFrame>

<style scoped>
.practical-note {
  max-width: 30rem;
}
</style>

<!--
Copilot is not only autocomplete.

In practice, it works through the context it sees, the instructions that receives, 
the policies that enable or disable features, and the workflow we expect people to follow.

The result depends on the environment we create around it.

So rollout is not one switch.

It is a system we shape on purpose.
-->
