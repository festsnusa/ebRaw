<template>
  <div class="header">
    <NuxtLink>
      <img src="@/assets/images/logo.png" alt="logo" />
    </NuxtLink>
    <Navigation />
    <Account />
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.header {
  padding: 2rem 5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 1px 3px 8px -5px rgba(34, 60, 80, 0.2);
}
</style>