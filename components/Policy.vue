<template>
  <div class="policy">
    <div class="policy__card" v-for="(card, i) in cards" :key="`policy__${i}`">
      <img class="policy__image" :src="images[card.img]" alt="icon">
      <p class="policy__title">{{ card.title }}</p>
      <p class="policy__subtitle">{{ card.subtitle }}</p>
    </div>
  </div>
</template>

<script setup>
import { filename } from 'pathe/utils';
const glob = import.meta.glob('~/assets/images/policy/*.svg', { eager: true });
const images = Object.fromEntries(
  Object.entries(glob).map(([key, value]) => [filename(key), value.default])
);

const cards = [
  { "title": "Free Shipping", "subtitle": "Orders over $200", "img": "1" },
  { "title": "Secure Payment", "subtitle": "100% secure payment", "img": "2" },
  { "title": "Gift Certificate", "subtitle": "Buy now $500 to $1000", "img": "3" },
  { "title": "24/7 Support", "subtitle": "Ready support", "img": "4" },
]
</script>

<style scoped lang="scss">
.policy {
  padding: 5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: center;

  &__card {
    padding: 3rem;
    border: 1px solid #CCCCCC;
    min-width: 270px;

    &:hover {
      box-shadow: 0px 0px 24px 0px rgba(34, 60, 80, 0.2);
      border: none;

      img {}
    }
  }

  &__image {
    padding: 1rem;
    background-color: #E5E5E5;
  }

  &__title {
    font-weight: 600;
    font-size: 24px;
    line-height: 34.68px;
  }

  &__subtitle {
    font-weight: 400;
    font-size: 14px;
    line-height: 20.23px;
  }
}
</style>