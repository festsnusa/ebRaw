<template>
  <div class="review">
    <div class="review__overlay"></div>
    <div class="review__content">
      <h1 class="review__title">What Say Our Regular Customer</h1>
      <swiper-container class="swiper" navigation="true" :slides-per-view="1" :space-between="10"
        :pagination="{ clickable: true }">
        <swiper-slide class="review__slider" v-for="(item, i) in items" :key="`review__${i}`">
          <p class="review__snippet">{{ item.snippet }}</p>
          <p class="review__text">{{ item.text }}</p>
          <div class="review__hero">
            <img :src="images[item.avatar]" alt="avatar">
            <span>{{ item.name }}</span>
            <span>{{ item.position }}</span>
          </div>

        </swiper-slide>
      </swiper-container>
    </div>
  </div>
</template>

<script setup>
import { filename } from 'pathe/utils';
const glob = import.meta.glob('~/assets/images/*.png', { eager: true });
const images = Object.fromEntries(
  Object.entries(glob).map(([key, value]) => [filename(key), value.default])
);

const items = [
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
  { "snippet": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour", "text": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "avatar": "avatar-wade", "name": "Wade Warren", "position": "UI designer" },
]
</script>

<style scoped lang="scss">
.review {
  padding: 7rem;
  text-align: center;
  position: relative;
  background-image: url('@/assets/images/review-background.png');
  background-size: cover;
  color: #fff;

  &__overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('@/assets/images/overlay.png');
    background-size: cover;
    background-position: center;
    opacity: 0.75;
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  &__slider {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    padding: 4rem;
  }

  &__title {
    font-weight: 600;
    font-size: 30px;
    line-height: 43.35px;
    color: #fff;
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

  &__hero {
    display: flex;
    flex-direction: column;

    img {
      padding: 1rem;
    }
  }
}
</style>