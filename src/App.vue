<script setup>
import Header from './components/layout/Header.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Products from './components/Products.vue';
</script>

<template>
  <div class="container">
    <Header />
    <Hero />
    <About />
    <Products />
  </div>
</template>

<style lang="scss" scoped>
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/clash-display');

.container {
  font-family: 'Satoshi', sans-serif;
  max-width: 1440px;
  margin: auto;
}
</style>
