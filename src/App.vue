<script setup lang="ts">
import CursorArea from './components/CursorArea.vue'

const CATEGORIES = {
  general: 'General',
  linkAndStatus: 'Links & status',
  selection: 'Selection',
  dragAndDrop: 'Drag & drop',
  resizingAndScrolling: 'Resizing & scrolling',
  zooming: 'Zooming',
}

const items = [
  {
    type: 'auto',
    category: CATEGORIES.general,
  },
  {
    type: 'default',
    category: CATEGORIES.general,
  },
  {
    type: 'none',
    category: CATEGORIES.general,
  },
  {
    type: 'context-menu',
    category: CATEGORIES.linkAndStatus,
  },
  {
    type: 'help',
    category: CATEGORIES.linkAndStatus,
  },
  {
    type: 'pointer',
    category: CATEGORIES.linkAndStatus,
  },
  {
    type: 'progress',
    category: CATEGORIES.linkAndStatus,
  },
  {
    type: 'wait',
    category: CATEGORIES.linkAndStatus,
  },
  {
    type: 'cell',
    category: CATEGORIES.selection,
  },
  {
    type: 'crosshair',
    category: CATEGORIES.selection,
  },
  {
    type: 'text',
    category: CATEGORIES.selection,
  },
  {
    type: 'vertical-text',
    category: CATEGORIES.selection,
  },
  {
    type: 'alias',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'copy',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'move',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'no-drop',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'not-allowed',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'grab',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'grabbing',
    category: CATEGORIES.dragAndDrop,
  },
  {
    type: 'all-scroll',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'col-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'row-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'n-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'e-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 's-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'w-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'ne-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'nw-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'se-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'sw-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'ew-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'ns-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'nesw-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'nwse-resize',
    category: CATEGORIES.resizingAndScrolling,
  },
  {
    type: 'zoom-in',
    category: CATEGORIES.zooming,
  },
  {
    type: 'zoom-out',
    category: CATEGORIES.zooming,
  }
]
</script>

<template>
  <div class="wrapper">
    <h1 class="heading">Which cursor type do you like?</h1>
    <CursorArea
      v-for="(item, i) in items"
      :key="item.type"
      :color="i % 2 === 0 ? '#E5D9F2' : '#F5EFFF'"
      :cursor-type="item.type"
      :category="item.category"
    />
  </div>
</template>

<style scoped>
.heading {
  text-align: center;
  padding: 0.2rem 0 1.4rem;
  font-size: 2rem;
  margin: 0;
}
</style>
