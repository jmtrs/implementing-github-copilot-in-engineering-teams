<script setup lang="ts">
defineProps<{
  micro?: string
  grid?: boolean
  split?: boolean
  reverse?: boolean
  shellClass?: string
}>()
</script>

<template>
  <div class="deck-shell" :class="[shellClass]">
    <div class="muted-grid"></div>
    <div
      v-if="grid"
      class="deck-grid"
      :class="{
        split,
        'split-reverse': reverse,
      }"
    >
      <slot />
    </div>
    <template v-else>
      <slot />
    </template>
    <p v-if="micro" class="slide-micro fade-in" style="animation-delay: 1.45s">{{ micro }}</p>
  </div>
</template>
