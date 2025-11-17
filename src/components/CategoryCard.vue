<template>
  <div class="category-card">
    <img :src="image" :alt="title" class="category-image" />
    <h3 class="category-title">{{ title }}</h3>
    <p class="category-count">{{ itemCount }} items</p>
  </div>
</template>

<script setup>
defineProps({
  image: String,
  title: String,
  itemCount: Number,
});
</script>

<style scoped>
.category-card {
  width: 130px;
  padding: 15px;
  box-sizing: border-box;
  background-color: #fef7f4;
  border-radius: 12px;
  text-align: center;
  font-family: Arial, sans-serif;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
}
.category-image {
  width: 80px;
  height: 80px;
  object-fit: contain;
  margin-bottom: 10px;
}
.category-title {
  font-size: 1.1rem;
  font-weight: bold;
  color: #37475A;
  margin: 8px 0 4px 0;
}
.category-count {
  font-size: 0.9rem;
  color: #a0a0a0;
  margin: 0;
}
</style>