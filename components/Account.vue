<template>
  <div class="account">
    <img class="account__search" src="@/assets/images/search.svg" alt="search">
    <div class="account__cart">
      <span class="account__count">{{ count }}</span>
      <img class="account__bag" src="@/assets/images/cart.svg" alt="cart">
    </div>
    <img class="account__favorite" src="@/assets/images/favorite.svg">
    <button class="account__button">
      <img src="@/assets/images/avatar.svg" alt="avatar">
      <span>Genesis Harper</span>
    </button>
  </div>
</template>

<script setup lang="ts">
const count = ref(0)
</script>

<style scoped lang="scss">
.account {
  display: flex;
  align-items: center;
  gap: 2rem;

  &__cart {
    position: relative;
  }

  &__count {
    position: absolute;
    bottom: 1.25rem;
    background-color: #073046;
    color: #fff;
    border-radius: 50%;
    padding: 0.2rem 0.5rem
  }

  &__button {
    display: flex;
    align-items: center;
    gap: 1rem;
    background-color: #073046;
    border-radius: 5px;
    padding: 1rem;
    color: #fff;
    font-weight: 600;
    font-size: 13px;
  }
}
</style>