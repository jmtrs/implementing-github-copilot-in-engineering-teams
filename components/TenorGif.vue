<script setup>
import { onMounted, nextTick } from 'vue'

defineProps({
  postid: { type: String, required: true },
  aspectRatio: { type: String, default: '1' },
  width: { type: String, default: '130px' },
  bottom: { type: String, default: '20px' },
  right: { type: String, default: '28px' },
  delay: { type: String, default: '2s' },
})

onMounted(async () => {
  await nextTick()
  const existing = document.querySelector('script[src*="tenor.com/embed.js"]')
  if (existing) existing.remove()
  const s = document.createElement('script')
  s.src = 'https://tenor.com/embed.js'
  s.async = true
  document.body.appendChild(s)
})
</script>

<template>
  <div class="tenor-wrap" :style="{ width, bottom, right, animationDelay: delay }">
    <div
      class="tenor-gif-embed"
      :data-postid="postid"
      data-share-method="host"
      :data-aspect-ratio="aspectRatio"
      data-width="100%"
    />
  </div>
</template>

<style scoped>
.tenor-wrap {
  position: absolute;
  pointer-events: none;
  opacity: 0;
  animation: tenor-appear 0.6s ease forwards;
}

@keyframes tenor-appear {
  from { opacity: 0; transform: scale(0.85); }
  to   { opacity: 1; transform: scale(1); }
}
</style>
