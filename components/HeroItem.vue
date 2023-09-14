<template>
  <div class="hero-item">
    <div class="left">
      <img src="@/assets/images/cocktail-dress.png" alt="hero-item">
    </div>
    <div class="right">
      <span class="title">{{ title }}</span>
      <div class="price">
        <span class="price--new">${{ price }}</span>
        <span class="price--old">${{ oldPrice }}</span>
      </div>
      <button>Add to cart</button>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  title: {
    type: String,
  },
  price: {
    type: Number,
  },
  oldPrice: {
    type: Number,
  },
})
</script>

<style scoped lang="scss">
.hero-item {
  position: absolute;
  right: 50%;
  bottom: 20%;
  padding: 1rem 2rem;
  box-shadow: 0px 7px 8px 0px rgba(34, 60, 80, 0.2);

  display: flex;
  align-items: center;
  gap: 1rem;

  button {
    text-transform: uppercase;
    padding: 1rem 2rem;
    background-color: #073046;
    color: #fff;
  }

  &:after {
    content: "";
    width: 100px;
    height: 100px;
    background-image: url('../assets/images/hot.svg');
    background-size: cover;
    position: absolute;
    top: -20%;
    right: -15%;
  }
}

.title {
  font-weight: 600;
  font-size: 24px;
  line-height: 31.08px;
  max-width: 130px;
}

.right {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.price {
  display: flex;
  gap: 1rem;
  font-weight: 500;

  &--old {
    text-decoration: line-through;
    color: #A1A1A1;
  }
}
</style>