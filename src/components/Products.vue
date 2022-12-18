<template>
  <div class="products">
    <div class="products__container">
      <Product
        class="product"
        v-for="product in products"
        :key="product.id"
        :img="product.img"
        :name="product.name"
        :price="product.price"
      />
    </div>
    <Button
      path="/"
      class="products__link"
      type="link"
      color="secondary"
      >View collection</Button
    >
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Product from '@/components/Product.vue';
import Button from '@/components/UI/Button.vue';

const products = ref([
  {
    id: 1,
    img: '/products/dandy-chair.png',
    name: 'The Dandy Chair',
    price: 250,
  },
  {
    id: 2,
    img: '/products/rustic-vase-set.png',
    name: 'Rustic Vase Set',
    price: 155,
  },
  {
    id: 3,
    img: '/products/silky-vase.png',
    name: 'The Silky Vase',
    price: 125,
  },
  {
    id: 4,
    img: '/products/lucy-lamp.png',
    name: 'The Lucy Lamp',
    price: 400,
  },
]);
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.products {
  display: flex;
  flex-direction: column;

  &__container {
    box-sizing: border-box;
    display: flex;
    margin: 30px 80px 50px;
    column-gap: 20px;
  }

  &__link {
    font-size: 16px;
    line-height: 150%;
    align-self: baseline;
    margin: 0 auto 40px;
    text-align: center;
  }
}
</style>
