<script setup>
import DropDownMenu from './components//DropDownMenu.vue'
import DropDownItem from './components//DropDownItem.vue'
</script>

<template>
  <DropDownMenu>
    <template #default="{ handleClick }">
      <DropDownItem :handleClick="handleClick" item="Item 1">Option 1</DropDownItem>
      <DropDownItem :handleClick="handleClick" item="Item 2">Option 2</DropDownItem>
      <DropDownItem :handleClick="handleClick" item="Item 3">Option 3</DropDownItem>
    </template>
  </DropDownMenu>
</template>

<style scoped>
</style>
