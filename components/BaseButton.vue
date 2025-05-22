<template>
  <NuxtLink  class="app-button" :style="{ backgroundColor: bgColor }" :to="to">
    {{ label }}
  </NuxtLink>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    required: true
  },
  bgColor: {
    type: String,
    default: '#FEF0C1'
  },
  hoverColor: {
    type: String,
    default: '#FAECD6'
  },
  to: {
    type: String,
    default: '/'
  }
});
</script>

<style scoped>
.app-button {
  border: none;
  border-radius: 5px;
  padding: 1rem 4rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  font-family: 'Inter', sans-serif;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  text-decoration: none;
  color: #25424C;
  transition: transform 0.5s ease, background-color 0.3s ease;
}

.app-button:hover {
  background-color: v-bind(hoverColor);
  transform: scale(1.05);
}
</style>

