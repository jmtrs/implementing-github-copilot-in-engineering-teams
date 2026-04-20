<script setup lang="ts">
defineProps<{
  kicker?: string
  title: string
  titleClass?: string
  kickerDelay?: string
  titleDelay?: string
}>()
</script>

<template>
  <div>
    <p v-if="kicker" class="deck-kicker fade-up" :style="{ animationDelay: kickerDelay || '0.12s' }">{{ kicker }}</p>
    <h1 class="deck-title fade-up" :class="titleClass" :style="{ animationDelay: titleDelay || '0.26s' }">{{ title }}</h1>
  </div>
</template>
