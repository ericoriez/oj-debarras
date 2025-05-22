<template>
  <div class="base-detailed-card-container">
    <div class="base-detailed-card">
      <h4>{{ title }}</h4>
      <img :src="imageSrc" :alt="title" :style="{ width: imageWidth }"/>
      <p>
        {{ text }}
      </p>
    </div>
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
    },
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.base-detailed-card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;

}

.base-detailed-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  font-family: 'Inter', sans-serif;
  color: #25424C;
  font-size: 24px;
}

.base-detailed-card img:hover {
  transform: scale(1.05);
}

.base-detailed-card img {
  height: 250px;
  object-fit: cover;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  transition: transform 0.5s ease;

}
.base-detailed-card p {
  text-align: center;
  width: 300px;
}
.base-detailed-card h4 {
  margin-top: 10px;
  text-align: center;
}
</style>
