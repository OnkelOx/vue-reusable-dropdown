<script setup>
const handleClick = (data, textContent) => {
  console.log('Clicked item:', data)
  console.log('Clicked item text:', textContent)
}
</script>

<template>
  <div class="dropdown">
    <button class="dropbtn">
      <p>Dropdown</p>
    </button>
    <div class="dropdown-content">
      <slot :handleClick="handleClick"></slot>
    </div>
  </div>
</template>

<style scoped>
.dropbtn {
  background-color: var(--element);
  width: 100%;
  padding: 8px;
}

.dropdown {
  margin: 2px;
  background-color: var(--element);
  width: 200px;
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: var(--light);
  width: 100%;
  z-index: 1;
}

.dropdown-content a {
  color: var(--text);
  display: block;
}

.dropdown-content a:hover {
  background-color: var(--highlight);
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>