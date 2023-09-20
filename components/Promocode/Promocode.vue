<template>
  <div class="promocode">
    <div class="promocode__overlay"></div>
    <div class="promocode__content">
      <PromocodeGift />
      <PromocodeProduct />
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.promocode {
  position: relative;
  background-image: url('@/assets/images/clark-street.png');
  background-size: cover;
  padding: 6rem;
  display: flex;

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
    justify-content: space-between;
    width: 100%;
    gap: 10rem;
  }
}
</style>