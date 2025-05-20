<template>
  <div class="base-card">
    <img :src="imageSrc" :alt="title" :style="{ width: imageWidth }" />
    <h4>{{ title }}</h4>
  </div>
</template>

<script>

export default {
  name: 'BaseCard',
  props: {
    title: {
      type: String,
      required: true
    },
    imageSrc: {
      type: String,
      required: true
    },
    imageWidth: {
      type: String,
      default: '250px'
    }
  }
}
</script>

<style scoped>
.base-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px;
}

.base-card img {
  height: 250px;
  object-fit: cover;
}

.base-card h4 {
  margin-top: 10px;
  text-align: center;
}
</style>
