<template>
  <div class="promo-card" :style="{ backgroundColor: bgColor }">
    <div class="promo-text">
      <h2 class="promo-title">{{ title }}</h2>
      <p class="promo-subtitle">{{ subtitle }}</p>
      <ButtonComponent :variant="buttonVariant">
        Shop Now
      </ButtonComponent>
    </div>
    <div class="promo-image-container">
      <img :src="image" :alt="title" class="promo-image" />
    </div>
  </div>
</template>

<script setup>
import ButtonComponent from './ButtonComponent.vue';

defineProps({
  title: String,
  subtitle: String,
  image: String,
  buttonVariant: String,
  bgColor: String,
});
</script>

<style scoped>
.promo-card {
  flex: 1;
  min-width: 300px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-radius: 10px;
  padding: 25px;
  font-family: Arial, sans-serif;
  box-sizing: border-box;
}
.promo-text {
  flex: 1;
}
.promo-title {
  font-size: 1.6rem;
  font-weight: bold;
  color: #222;
  margin: 0 0 5px 0;
  line-height: 1.2;
}
.promo-subtitle {
  font-size: 1rem;
  color: #555;
  margin: 0 0 15px 0;
}
.promo-image-container {
  flex-shrink: 0;
  padding-left: 20px;
}
.promo-image {
  max-width: 160px;
  height: auto;
}
</style>