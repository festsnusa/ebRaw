<template>
  <div class="product" @mouseover="isVisible = true" @mouseleave="isVisible = false">
    <div class="product__additional">
      <span class="product__sale" v-if="item.sale">Sale</span>
      <div class="product__favorite" v-show="isVisible">
        <img src="@/assets/images/favorite.svg" alt="favorite">
      </div>
      <div class="product__link" v-show="isVisible">
        <img src="@/assets/images/link.svg" alt="link">
      </div>
      <div class="product__search" v-show="isVisible">
        <img src="@/assets/images/search.svg" alt="search">
      </div>
    </div>

    <img :src="`/_nuxt/assets/images/products/${item.image}.png`" alt="product">
    <span class="product__title">{{ item.title }}</span>
    <span class="product__price">${{ item.price }}</span>
    <div class="product__footer" v-show="isVisible">
      <button>
        <img src="@/assets/images/cart.svg" alt="cart">
        <span class="product__add">Add to bag</span>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
const isVisible = ref(false)

const props = defineProps({
  item: {
    type: Object,
    required: true,
  }
})
</script>

<style scoped lang="scss">
.product {
  position: relative;
  padding-top: 1rem;
  border: 1px solid #CCCCCC;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;

  &:hover {
    transform: scale(1.02);
    transition: all 0.2s ease-in-out;
  }

  &__additional {
    position: absolute;
    right: 1rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  &__favorite,
  &__link,
  &__search {
    border: 1px solid #023047;
    padding: 0.5rem;
    display: flex;
    justify-content: center;
  }

  &__link {
    background-color: #073046;
  }

  &__title {
    font-weight: 500;
    font-size: 18px;
    line-height: 24.21px;
  }

  &__add,
  &__sale {
    text-transform: uppercase;
  }

  &__sale {
    // position: absolute;
    // right: 1rem;
    border: 1px solid #023047;
    padding: 0.5rem 1rem;
    color: #023047;
  }

  &__footer {
    background-color: #023047;
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 2rem;

    button {
      display: flex;
      align-items: center;
      background-color: #fff;
      padding: 1rem 2rem;
    }
  }
}
</style>