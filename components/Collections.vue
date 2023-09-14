<template>
  <div class="collections">
    <div class="collections__new collection">
      <div class="left">
        <img src="@/assets/images/woman__new.png" alt="woman__new">
      </div>
      <div class="right">
        <span class="right__extra">Get Extra 50% Off</span>
        <h1 class="right__title">New Woman Collection</h1>
        <span class="right__special">Special Promo</span>
        <button>Find Collection</button>
      </div>
    </div>
    <div class="collections__bags collection">
      <img src="@/assets/images/bag.png" alt="bag">
      <span>70% Off On</span>
      <h1>Woman Bags Collection</h1>
      <button>Shop Now</button>
    </div>
    <div class="collections__mackup collection">
      <img src="@/assets/images/makeup.png" alt="mackup">
      <span>70% Off On</span>
      <h1>Woman Bags Collection</h1>
      <button>Shop Now</button>
    </div>
    <div class="collections__watch collection">
      <img src="@/assets/images/woman__watch.png" alt="mackup">
      <span>30-60% Off On</span>
      <h1>Woman Watch Collection</h1>
      <button>Shop Now</button>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
button {
  font-weight: 400;
  font-size: 14px;
  line-height: 20.23px;
  border: 1px solid #666666;
  padding: 1rem 2rem;

  &:hover {
    background-color: #073046;
    color: #fff;
  }
}

.collection {
  background-color: #fff;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  // padding: 1rem;
  align-items: center;
  justify-content: center;

  &:nth-child(1) {
    grid-area: one;
  }

  &:nth-child(2) {
    grid-area: two;
  }

  &:nth-child(3) {
    grid-area: three;
  }

  &:nth-child(4) {
    grid-area: four;

    img {
      width: 100%;
    }

  }

  &:hover {
    box-shadow: 0px 0px 11px 7px rgba(34, 60, 80, 0.2);
  }
}

.collections {
  display: grid;
  grid-template-areas:
    "one one four"
    "two three four";
  grid-gap: 2rem;
  padding: 0 5rem;
  background-color: #F5F5F5;

  &__new {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 2rem;
    padding: 0 3rem;


  }
}

.right {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;

  &__extra {
    font-weight: 500;
    font-size: 20px;
    line-height: 28.9px;
  }

  &__title {
    font-size: 30px;
    font-weight: 600;
    line-height: 43.35px;
  }

  &__special {
    font-weight: 500;
    font-size: 20px;
    line-height: 28.9px;
  }
}
</style>