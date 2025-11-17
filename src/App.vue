<template>
  <main class="page-container">
    
    <section class="category-section">
      <CategoryCard
        v-for="category in categories"
        :key="category.title"
        :title="category.title"
        :itemCount="category.items"
        :image="category.img"
      />
    </section>

    <section class="promotion-section">
      <PromotionCard
        v-for="promo in promotions"
        :key="promo.title"
        :title="promo.title"
        :subtitle="promo.subtitle"
        :image="promo.img"
        :buttonVariant="promo.btnType"
        :bgColor="promo.bgColor"
      />
    </section>

  </main>
</template>

<script setup>
import CategoryCard from './components/CategoryCard.vue';
import PromotionCard from './components/PromotionCard.vue';

import catImg1 from '@/assets/images/image.png';
import catImg2 from '@/assets/images/image copy 2.png';
import catImg3 from '@/assets/images/image copy 3.png';
import catImg4 from '@/assets/images/image copy 4.png';
import catImg5 from '@/assets/images/image copy 5.png';
import catImg6 from '@/assets/images/image copy 6.png';
import catImg7 from '@/assets/images/image copy 7.png';
import catImg8 from '@/assets/images/image copy 8.png';
import catImg9 from '@/assets/images/image copy 9.png';

import promoImg1 from '@/assets/images/image copy 10.png';
import promoImg2 from '@/assets/images/image copy 11.png';
import promoImg3 from '@/assets/images/image copy 12.png';

const categories = [
  { img: catImg1, title: 'Cake & Milk', items: 14 },
  { img: catImg2, title: 'Peach', items: 17 },
  { img: catImg3, title: 'Oganic Kiwi', items: 21 },
  { img: catImg4, title: 'Red Apple', items: 68 },
  { img: catImg5, title: 'Snack', items: 34 },
  { img: catImg6, title: 'Black plum', items: 25 },
  { img: catImg7, title: 'Vegetables', items: 65 },
  { img: catImg8, title: 'Headphone', items: 33 },
  { img: catImg9, title: 'Cake & Milk', items: 54 },
];

const promotions = [
  {
    title: 'Everyday Fresh &',
    subtitle: 'Clean with Our Products',
    img: promoImg1,
    btnType: 'green',
    bgColor: '#f0f4e8',
  },
  {
    title: 'Make your Breakfast',
    subtitle: 'Healthy and Easy',
    img: promoImg2,
    btnType: 'green',
    bgColor: '#fbe9eb',
  },
  {
    title: 'The best Organic',
    subtitle: 'Products Online',
    img: promoImg3,
    btnType: 'orange',
    bgColor: '#e6f3ff',
  },
];
</script>

<style>
body {
  font-family: Arial, sans-serif;
  background-color: #ffffff;
}

.page-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.category-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
  margin-bottom: 30px;
}

.promotion-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}
</style>