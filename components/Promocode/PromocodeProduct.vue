<template>
  <div class="product">
    <swiper-container navigation="true" :slides-per-view="1" :space-between="10">
      <swiper-slide class="product__slider" v-for="(item, i) in items" :key="`product__${i}`">
        <img src="@/assets/images/promocode.png" alt="promocode">
        <p class="product__title">{{ item.title }}</p>
        <span class="product__price">${{ item.price }}</span>
        <div class="product__stars">
          <PromocodeStar v-for="(n, j) in item.starsCount" :key="`star__${j}`" />
        </div>
      </swiper-slide>
    </swiper-container>
  </div>
</template>

<script setup>
const items = [
  { "title": "Ladies Hair Bands", "price": "150.00", "starsCount": 5 },
  { "title": "Ladies Hair Bands", "price": "130.00", "starsCount": 4 },
  { "title": "Ladies Hair Bands", "price": "125.00", "starsCount": 3 },
  { "title": "Ladies Hair Bands", "price": "110.00", "starsCount": 4 },
  { "title": "Ladies Hair Bands", "price": "105.00", "starsCount": 5 },
]
</script>

<style scoped lang="scss">
.product {

  position: relative;
  z-index: 5;

  &__slider {
    background-color: #fff;
    // position: absolute;
  }

  &__stars {
    display: flex;
  }
}
</style>