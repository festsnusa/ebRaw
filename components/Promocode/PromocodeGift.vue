<template>
  <div class="gift">
    <p class="gift__title">Gift voucher</p>
    <div class="gift__timer">
      <div class="gift__inputs">
        <input type="text" name="day" value="06" readonly>
        <input type="text" name="hours" value="18" readonly>
        <input type="text" name="minutes" value="29" readonly>
        <input type="text" name="seconds" value="35" readonly>
      </div>
      <div class="gift__labels">
        <label for="day">day</label>
        <label for="hours">hrs</label>
        <label for="minutes">mns</label>
        <label for="seconds">secs</label>
      </div>
    </div>
    <button class="gift__button">Copy Code</button>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
input {
  border: 2px solid #fff;
  color: #fff;
  background-color: transparent;
  font-weight: 600;
  font-family: Jost;
  font-size: 36px;
  padding: 0.5rem;
  width: 100%;
  text-align: center;
}

label {
  font-size: 14px;
  font-weight: 600;
  line-height: 18.83px;
  padding: 1rem;
}

.gift {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  color: #fff;
  backdrop-filter: blur(10px);
  padding: 7rem 6rem;
  width: 100%;
  text-align: center;

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

  &__inputs,
  &__labels {
    display: flex;
    gap: 2rem;
  }

  &__labels {
    justify-content: space-around;
  }

  &__button {
    padding: 1rem 2rem;
    color: #fff;
    border: 3px solid #fff;
    font-weight: 600;
    font-size: 14px;
    line-height: 18.83px;
    align-self: center;
  }

}
</style>