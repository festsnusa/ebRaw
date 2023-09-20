<template>
  <div class="partners">
    <div class="partners__text">
      <h1>Our Trusted Branding Partners</h1>
      <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some
        form, by injected humour.</p>
    </div>
    <swiper-container class="swiper" navigation="true" :slides-per-view="6" :space-between="10"
      :pagination="{ clickable: true }">
      <swiper-slide class="partners__slider" v-for="(item, i) in items" :key="`partners__${i}`">
        <img :src="`/_nuxt/assets/images/brands/${item}.png`" alt="partner">
      </swiper-slide>
    </swiper-container>

  </div>
</template>

<script setup lang="ts">
const items = [
  1, 2, 3, 4, 5, 6, 1, 3
]
</script>

<style scoped lang="scss">
.swiper {
  display: contents;
}

.partners {
  padding: 5rem;
  display: flex;
  flex-direction: column;
  align-items: center;

  &__text {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    text-align: center;

    p {
      max-width: 570px;
    }
  }

  &__slider {
    padding: 5rem 4rem;
  }
}
</style>