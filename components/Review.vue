<template>
  <div class="review">
    <h1 class="review__title">What Say Our Regular Customer</h1>
    <swiper-container class="swiper" navigation="true" :slides-per-view="1" :space-between="10"
      :pagination="{ clickable: true }">
      <swiper-slide class="review__slider" v-for="(item, i) in items" :key="`review__${i}`">
        <p class="review__snippet">{{ item.snippet }}</p>
        <p class="review__text">{{ item.text }}</p>
        <img :src="`/_nuxt/assets/images/${item.avatar}.png`" alt="avatar">
      </swiper-slide>
    </swiper-container>
  </div>
</template>

<script setup lang="ts">
const items = [
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
]
</script>

<style scoped lang="scss">
.review {
  text-align: center;


  &__slider {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
  }

  &__title {
    font-weight: 600;
    font-size: 30px;
    line-height: 43.35px;
  }

  &__snippet {
    font-weight: 400;
    font-size: 14px;
    line-height: 20.23px;
  }

  &__text {
    font-style: italic;
    font-size: 18px;
    font-weight: 400;
    max-width: 570px;
  }
}

// .swiper {
//   display: contents;
// }
</style>