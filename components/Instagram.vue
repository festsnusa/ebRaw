<template>
  <div class="instagram">
    <div class="instagram__header">
      <img class="instagram__logo" src="@/assets/images/instagram/instagram.png" alt="instagram">
      <h1 class="instagram__title">Follow us in instagram @graphic_raz</h1>
    </div>
    <div class="instagram__carousel">
      <div class="instagram__item" v-for="index in 4" :key="`item__${index}`">
        <img class="instagram__image" :src="`/_nuxt/assets/images/instagram/${index}.png`" alt="item">
        <div class="instagram__overlay">
          <img class="instagram__plus" src="../assets/images/instagram/plus.svg" alt="plus">
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
.instagram {
  padding: 7rem 0;
  background-color: #F5F5F5;
  text-align: center;

  &__header {
    padding: 2rem;
  }

  &__title {
    font-size: 30px;
    font-weight: 600;
    line-height: 54.45px;
  }

  &__carousel {
    display: flex;
  }

  &__item {
    display: flex;
    width: 100%;
    position: relative;

    &:hover {
      .instagram__overlay {
        opacity: 1;
      }
    }
  }

  &__image {
    // position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    opacity: 0;
    transition: opacity 0.3s ease;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__plus {
    padding: 2rem;
    cursor: pointer;
  }
}
</style>