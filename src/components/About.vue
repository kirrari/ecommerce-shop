<template>
  <div class="about">
    <h2 class="about__title">What makes our brand different</h2>
    <div class="about__items">
      <div
        class="about__item"
        v-for="(item, index) in aboutItems"
        :key="index"
      >
        <img
          :src="item.icon"
          :alt="item.name"
          class="about__icon"
        />
        <h3 class="about__name">{{ item.name }}</h3>
        <p class="about__description">{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const aboutItems = [
  {
    icon: '/about/icon-delivery.png',
    name: 'Next day as standard',
    description: 'Order before 3pm and get your order the next day as standard',
  },
  {
    icon: '/about/icon-checkmark.png',
    name: 'Made by true artisans',
    description:
      'Handmade crafted goods made with real passion and craftmanship',
  },
  {
    icon: '/about/icon-purchase.png',
    name: 'Unbeatable prices',
    description:
      'For our materials and quality you won’t find better prices anywhere',
  },
  {
    icon: '/about/icon-like.png',
    name: 'Recycled packaging',
    description:
      'We use 100% recycled to ensure our footprint is more manageable',
  },
];
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.about {
  &__title {
    display: block;
    font-family: $clash-display;
    font-weight: 400;
    font-size: 24px;
    line-height: 140%;
    color: $primary-dark;
    text-align: center;
    margin: 80px 0 0 0;
    @media (max-width: 1024px) {
      margin: 50px 20px;
    }
    @media (max-width: 1024px) {
      margin: 50px 20px 35px;
    }
  }

  &__items {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin: 35px 80px 80px;
    @media (max-width: 1145px) {
      grid-template-columns: repeat(2, 1fr);
    }
    @media (max-width: 1024px) {
      margin: 35px 40px 30px;
    }
    @media (max-width: 480px) {
      grid-template-columns: 1fr;
      margin: 35px 20px 40px;
    }
  }

  &__item {
    background: #f9f9f9;
    padding: 48px;
    display: flex;
    flex-direction: column;
    row-gap: 12px;
    @media (max-width: 767px) {
      padding: 24px;
    }
  }

  &__icon {
    width: 24px;
    height: 24px;
  }

  &__name {
    font-weight: 400;
    font-size: 20px;
    line-height: 140%;
    color: $primary-dark;
  }

  &__description {
    font-size: 16px;
    line-height: 150%;
    color: $primary-dark;
  }
}
</style>
