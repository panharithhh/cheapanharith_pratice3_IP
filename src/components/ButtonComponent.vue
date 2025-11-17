<template>
  <button :class="['shop-btn', variant]">
    <slot /> &rarr;
  </button>
</template>

<script setup>
defineProps({
  variant: {
    type: String,
    default: 'green',
  },
});
</script>

<style scoped>
.shop-btn {
  padding: 10px 18px;
  border: none;
  border-radius: 6px;
  color: white;
  font-size: 0.9rem;
  font-weight: bold;
  cursor: pointer;
  transition: opacity 0.2s ease;
}
.shop-btn:hover {
  opacity: 0.8;
}
.shop-btn.green {
  background-color: #28a745;
}
.shop-btn.orange {
  background-color: #fd7e14;
}
</style>