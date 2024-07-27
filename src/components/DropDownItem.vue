<script setup>
const props = defineProps({
  handleClick: {
    type: Function,
    required: true
  },
  item: {
    type: String,
    required: true
  }
})

function handleClick(event) {
  props.handleClick(props.item, event.target.textContent.trim())
}
</script>

<template>
  <div class="item" @click="handleClick">
    <slot></slot>
  </div>
</template>

<style scoped>
.item {
  cursor: pointer;
  padding: 8px;
}
</style>