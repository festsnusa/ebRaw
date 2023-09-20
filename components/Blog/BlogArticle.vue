<template>
  <div class="posts">
    <div class="post" v-for="(post, i) in posts" :key="`post__${i}`">
      <span class="post__tag">{{ post.tag }}</span>
      <img class="post__image" :src="images[post.img]" alt="background">
      <div class="post__content">
        <span class="post__date">Design July 11, 2021</span>
        <p class="post__title">{{ post.title }}</p>
        <p class="post__subtitle">{{ post.subtitle }}</p>
        <button class="post__button">Read More</button>
      </div>

    </div>

  </div>
</template>

<script setup>
import { filename } from 'pathe/utils';
const glob = import.meta.glob('~/assets/images/blog/*.png', { eager: true });
const images = Object.fromEntries(
  Object.entries(glob).map(([key, value]) => [filename(key), value.default])
);

const posts = [
  { "title": "2021’S Biggest Sneaker Is Getting Us So Pumped For Summer", "subtitle": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "tag": "Sale", "img": 1 },
  { "title": "2021’S Biggest Sneaker Is Getting Us So Pumped For Summer", "subtitle": "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable.", "tag": "Fashion", "img": 2 }
]
</script>

<style scoped lang="scss">
.posts {
  display: flex;
  flex: 1;
  gap: 3.5rem;
}

.post {
  position: relative;
  flex: 1;

  &:hover {
    background-color: #fff;
  }

  &__tag {
    position: absolute;
    color: #fff;
    padding: 1.5rem;
    font-size: 14px;
    font-weight: 500;
    line-height: 20.23px;
  }

  &__image {
    width: 100%;
  }

  &__date {
    font-weight: 500;
    font-size: 10px;
    line-height: 14.45px;
    text-transform: uppercase;
  }

  &__title {
    font-weight: 500;
    font-size: 18px;
    line-height: 25.47px;
    color: #333333;
    text-decoration: underline;
  }

  &__subtitle {
    font-weight: 400;
    font-size: 14px;
    line-height: 20.23px;
    color: #666666;
  }

  &__button {
    padding: 1rem 2rem;
    border: 1px solid #666666;
    color: #666666;
    font-size: 14px;
    font-weight: 500;

    &:hover {
      background-color: #073046;
      color: #fff;
    }
  }

  &__content {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: flex-start;
  }
}
</style>