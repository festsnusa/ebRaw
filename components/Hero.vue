<template>
  <div class="hero">
    <swiper-container navigation="true" :slides-per-view="1" :space-between="50" :pagination="{ clickable: true }">
      <swiper-slide class="hero__slider" v-for="(item, i) in items" :key="`sauce__${i}`">
        <div class="left">
          <span>Trends Stock!</span>
          <h1>Short top keep you pretty</h1>
          <button>Shop now</button>
        </div>
        <div class="right"></div>
        <img class="hero__banner" src="@/assets/images/banner.png" alt="banner">

      </swiper-slide>
    </swiper-container>
  </div>
</template>

<script setup lang="ts">
import { register } from "swiper/element/bundle";
register();

const items = [
  { "title": "Solid color Sleeves", "price": "100", "oldPrice": "130" },
  { "title": "Solid color Sleeves", "price": "100", "oldPrice": "130" },
  { "title": "Solid color Sleeves", "price": "100", "oldPrice": "130" },
]
</script>

<style scoped lang="scss">
.hero {

  &__slider {}
}
</style>