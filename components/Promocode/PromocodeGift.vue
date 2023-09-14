<template>
  <div class="gift">
    <p class="gift__title">Gift voucher</p>
    <div class="gift__timer">
      <label for="day">day</label>
      <input type="text" name="day" value="06" readonly>
      <label for="hours">hrs</label>
      <input type="text" name="hours" value="18" readonly>
      <label for="minutes">mns</label>
      <input type="text" name="minutes" value="29" readonly>
      <label for="seconds">secs</label>
      <input type="text" name="seconds" value="35" readonly>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
input {
  border: none;
}

.gift {
  z-index: 5;
  color: #fff;
  backdrop-filter: blur(10px);
  padding: 4rem;

  &__title,
  &__timer {
    text-transform: uppercase;
  }

  &__title {
    font-weight: 600;
    font-size: 36px;
    line-height: 48.42px;
    border: 3px solid #fff;
    padding: 1rem 1.5rem;
  }

}
</style>