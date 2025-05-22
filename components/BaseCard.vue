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

.base-card img:hover {
  transform: scale(1.05);
}

.base-card img {
  height: 250px;
  object-fit: cover;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  transition: transform 0.5s ease;

}

.base-card h4 {
  margin-top: 10px;
  text-align: center;
}
</style>
