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
.about {
  &__title {
    font-family: 'Clash Display', sans-serif;
    font-weight: 400;
    font-size: 24px;
    line-height: 140%;
    color: #2a254b;
    text-align: center;
    margin: 80px 0 0 0;
  }

  &__items {
    display: flex;
    column-gap: 20px;
    margin: 35px 40px 80px;
  }

  &__item {
    background: #f9f9f9;
    padding: 48px;
    display: flex;
    flex-direction: column;
    row-gap: 12px;
    max-width: 25%;
  }

  &__icon {
    width: 24px;
    height: 24px;
  }

  &__name {
    font-weight: 400;
    font-size: 20px;
    line-height: 140%;
    color: #2a254b;
  }

  &__description {
    font-size: 16px;
    line-height: 150%;
    color: #2a254b;
  }
}
</style>
