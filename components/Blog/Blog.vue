<template>
  <div class="blog">
    <div class="blog__headline">
      <h1>Latest News</h1>
      <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some
        form, by injected humour</p>
    </div>
    <BlogArticle />

  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.blog {
  padding: 4rem 5rem;
  background-color: #F5F5F5;

  &__headline {
    text-align: center;
    padding-bottom: 5rem;
  }
}
</style>