<template>
  <ul class="navigation">
    <li class="navigation__item" v-for="(item, i) in arr" :key="`navigation__${i}`">
      <NuxtLink :to="item.link">
        {{ item.title }}
      </NuxtLink>
    </li>
  </ul>
</template>

<script setup lang="ts">
const arr = [
  { "title": "Home", "link": "/" },
  { "title": "Shop", "link": "/shop/" },
  { "title": "Product", "link": "/product/" },
  { "title": "Page", "link": "/page/" },
  { "title": "Blog", "link": "/blog/" }
]
</script>

<style scoped lang="scss">
.navigation {
  display: flex;
  gap: 2rem;
  align-items: center;
}
</style>