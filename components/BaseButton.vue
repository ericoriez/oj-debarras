<template>
  <button
      class="app-button"
      :style="{ backgroundColor: bgColor }"
  >
    {{ label }}
  </button>
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
  }
});
</script>

<style scoped>
.app-button {
  border: none;
  border-radius: 5px;
  padding: 1rem 4rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.app-button:hover {
  background-color: v-bind(hoverColor);
}
</style>

