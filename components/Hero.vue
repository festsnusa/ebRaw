<template>
  <div class="hero">
    <swiper-container navigation="true" :slides-per-view="1" :space-between="50" :pagination="{ clickable: true }">
      <swiper-slide class="hero__slider" v-for="(item, i) in items" :key="`sauce__${i}`">
        <div class="hero__description">
          <span>Trends Stock!</span>
          <h1 class="hero__title--top">Short top</h1>
          <h1 class="hero__title--bottom">keep you pretty</h1>
          <button class="hero__button">Shop now</button>
        </div>
        <HeroItem title="Solid Color Sleeves" :price="100" :oldPrice="130" />
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
h1 {
  text-transform: uppercase;
}

.hero {

  padding: 0 4rem;
  box-shadow: 0px 4px 8px 0px rgba(34, 60, 80, 0.2);

  &__slider {
    position: relative;
    padding: 0 4rem;
    display: flex;
    align-items: center;
  }

  &__title {
    &--top {
      font-weight: 500;
    }

    &--bottom {
      font-weight: 600;
    }
  }

  &__button {
    padding: 1rem 2rem;
    background-color: #073046;
    color: #fff;
    text-transform: uppercase;
  }
}
</style>