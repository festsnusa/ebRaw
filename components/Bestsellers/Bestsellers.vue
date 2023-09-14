<template>
  <div class="bestsellers">
    <div class="bestsellers__text">
      <h1>Best Selling Products</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna
        aliqua. Ut enim ad minim veniam.</p>
    </div>
    <swiper-container navigation="true" :slides-per-view="4" :space-between="50">
      <swiper-slide class="bestsellers__slider" v-for="(item, i) in  items " :key="`sauce__${i}`">
        <BestsellersProduct :item="item" />
      </swiper-slide>
    </swiper-container>

  </div>
</template>

<script setup lang="ts">
const items = [
  { "title": "Woman Sweet Hoodie", "price": "250.00", "sale": true, "image": 1 },
  { "title": "Woman Summer Hoodie", "price": "150.00", "sale": false, "image": 2 },
  { "title": "Winter Plush Warm Cotton", "price": "370.00", "sale": false, "image": 3 },
  { "title": "Women Cotton Shirts", "price": "150.00", "sale": false, "image": 4 },
  { "title": "Woman Sweet Hoodie", "price": "250.00", "sale": true, "image": 1 },
  { "title": "Woman Summer Hoodie", "price": "150.00", "sale": false, "image": 2 },
  { "title": "Winter Plush Warm Cotton", "price": "370.00", "sale": false, "image": 3 },
  { "title": "Women Cotton Shirts", "price": "150.00", "sale": false, "image": 4 },
]
</script>

<style scoped lang="scss">
.bestsellers {
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: 6rem;
  padding: 10rem 4rem;
  min-height: 854px;

  &__text {
    max-width: 542px;
    align-self: center;
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  &__slider {
    padding: 0 4rem;
  }
}
</style>