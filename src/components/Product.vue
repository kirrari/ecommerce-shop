<template>
  <div class="product">
    <router-link
      to="/"
      class="product__link"
    >
      <img
        :src="img"
        :alt="name"
        class="product__img"
      />
    </router-link>
    <router-link
      to="/"
      class="product__name"
      >{{ name }}</router-link
    >
    <p class="product__price">£{{ price }}</p>
  </div>
</template>

<script setup>
const props = defineProps({
  img: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.product {
  &__img {
    max-width: 305px;
    max-height: 375px;
    margin: 0 0 25px 0;
  }

  &__name {
    font-family: $clash-display;
    font-size: 20px;
    line-height: 140%;
    color: $primary-dark;
    text-decoration: none;
    margin: 0 0 10px 0;
  }

  &__price {
    font-size: 18px;
    line-height: 150%;
    color: $primary-dark;
  }
}
</style>
