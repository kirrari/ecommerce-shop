<script setup>
import Header from './components/layout/Header.vue';
</script>

<template>
  <div class="container">
    <Header />
  </div>
</template>

<style lang="scss" scoped>
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/clash-display');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.container {
  font-family: 'Satoshi', sans-serif;
  max-width: 1440px;
  margin: auto;
}
</style>
