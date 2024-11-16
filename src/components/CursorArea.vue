<script setup lang="ts">
defineProps<{ cursorType: string, color: string, category: string }>()
</script>

<template>
  <div class="cursor-area" :style="{ cursor: cursorType, backgroundColor: color }">
    <div>
      <h2 class="cursor-area__category">{{ category }}</h2>
      <span class="cursor-area__type">cursor: {{ cursorType }}</span>
    </div>
  </div>
</template>

<style scoped>
.cursor-area {
  height: 300px;
  display: grid;
  place-items: center;
}

.cursor-area__category {
  font-size: 1.2rem;
  margin-bottom: 0.2rem;
  color: #888;
}

.cursor-area__type {
  font-size: 1.4rem;
  color: #333;
  font-weight: bold;
}
</style>
