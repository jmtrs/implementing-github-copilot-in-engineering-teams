<script setup lang="ts">
const props = defineProps<{
  items: string[]
  startDelay?: number
  step?: number
  className?: string
}>()

const delayFor = (index: number) => `${(props.startDelay ?? 0.72) + index * (props.step ?? 0.24)}s`
</script>

<template>
  <div class="bullet-stack" :class="className">
    <p
      v-for="(item, index) in items"
      :key="item"
      class="bullet-row fade-up"
      :style="{ animationDelay: delayFor(index) }"
    >
      <span class="bullet-dot"></span>
      <span>{{ item }}</span>
    </p>
  </div>
</template>

<style scoped>
.bullet-stack {
  margin-top: 28px;
  display: grid;
  gap: 16px;
}

.bullet-row {
  margin: 0;
  display: grid;
  grid-template-columns: 18px 1fr;
  gap: 16px;
  font-size: 1.08rem;
  line-height: 1.55;
  color: #f5f5f5;
}

.bullet-dot {
  width: 8px;
  height: 8px;
  margin-top: 0.68em;
  border-radius: 999px;
  background: #f5f5f5;
}
</style>
