<template>
  <div class="footer">
    <div class="footer__content">
      <aside class="footer__aside">
        <img class="footer__logo" src="@/assets/images/logo.png" alt="logo">
        <p class="footer__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut
          labore.</p>
        <ul class="footer__links">
          <li class="footer__link" v-for="(social, i) in socials" :key="`socials__${i}`">
            <NuxtLink :to="social.link" target="_blank">
              <img :src="`/_nuxt/assets/images/socials/${social.title}.svg`" :alt="social.title">
            </NuxtLink>
          </li>
        </ul>
        <span class="footer__maps">Check our shop in Google Map</span>
      </aside>
      <nav class="footer__navigation">
        <ul v-for="(item, i) in navItems" :key="`navItems__${i}`">
          <p class="footer__navigation__title">{{ item.title }}</p>
          <li v-for="(title, j) in item.items" :key="`links__${j}`">
            <NuxtLink :to="`/${title.toLowerCase()}/`">
              {{ title }}
            </NuxtLink>
          </li>
        </ul>
      </nav>
      <form class="form" v-on:submit.prevent="onSubmit">
        <div class="form__header">
          <p class="form__title">Newsletter Signup</p>
          <p class="form__subtitle">There are many variations passages of Lorem Ipsum available</p>
        </div>
        <div class="form__content">
          <input class="form__input" type="email" placeholder="your email address">
          <button class="form__button">
            <img src="@/assets/images/arrow.svg" alt="arrow">
          </button>
        </div>
      </form>
    </div>
    <section class="footer__copyright">
      <p class="copyright__text">
        Copyright @2021 ebRaw. All Rights Reserved By Graphic Raz
      </p>
      <ul>
        <li v-for="(payment, i) in payments" :key="`payment__${i}`">
          <img :src="`/_nuxt/assets/images/payment/${payment}.png`" :alt="payment">
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup lang="ts">
const navItems = [
  { "title": "Support Links", "items": ["Product", "Guides", "Terms & Conditions", "Delivery", "Policy Privacy", "Policy Feedback"] },
  { "title": "Quick Links", "items": ["Product", "Guides", "Terms & Conditions", "Delivery", "Policy Privacy", "Policy Feedback"] },
  { "title": "Menu", "items": ["Product", "Guides", "Terms & Conditions", "Delivery", "Policy Privacy", "Policy Feedback"] },
]

const socials = [
  { "title": "facebook", "link": "https://www.facebook.com" },
  { "title": "twitter", "link": "https://www.twitter.com" },
  { "title": "instagram", "link": "https://www.instagram.com" },
  { "title": "linkedin", "link": "https://www.linkedin.com" }
]

const payments = ["paypal", "skrill", "visa", "mastercard", "americanexpress"]

const onSubmit = () => {

}
</script>

<style scoped lang="scss">
.footer {

  &__content {
    padding: 5rem;
    display: flex;
    justify-content: space-between;
    gap: 5rem;
  }

  &__aside {
    display: flex;
    flex: 20%;
    // max-width: 270px;
    flex-direction: column;
    align-items: flex-start;
    gap: 1rem;
  }

  &__navigation {
    display: flex;
    flex: 50%;
    justify-content: space-between;

    &__title {
      font-size: 18px;
      font-weight: 500;
      line-height: 28.89px;
    }

    li {
      font-weight: 400;
      font-size: 14px;
      line-height: 25.2px;
      color: #000;
    }
  }

  &__links {
    display: flex;
    gap: 1rem;
  }

  &__maps {
    text-decoration: underline;
    cursor: pointer;
  }

  &__copyright {
    background-color: #F3F3F3;
    padding: 2rem 5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;

    ul {
      display: flex;
      align-items: center;
      gap: 1rem;
    }
  }
}

.form {
  flex: 30%;
  display: flex;
  flex-direction: column;
  gap: 2rem;
  // position: relative;

  &__title {
    font-size: 18px;
    font-weight: 500;
    line-height: 28.89px;
  }

  &__subtitle {
    font-size: 14px;
    font-weight: 400;
    line-height: 22.47px;
  }

  &__content {
    position: relative;
    width: 70%;
  }

  &__input {
    padding: 2rem;
    width: 100%;
    font-size: 14px;
    font-family: Jost;
    color: #CCCCCC;
  }

  &__button {
    background-color: #073046;
    padding: 1rem;
    position: absolute;
    right: 1rem;
    top: 1rem;

  }
}
</style>