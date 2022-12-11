<template>
  <header class="header">
    <div class="header__top">
      <div class="header__menu--left">
        <a href="">
          <img
            class="header__search"
            src="../../assets/header/icon-search.svg"
          />
        </a>
      </div>
      <a
        href="#"
        class="header__title"
        >Avion</a
      >
      <div class="header__menu--right">
        <a href="">
          <img
            class="header__cart"
            src="../../assets/header/icon-cart.svg"
          />
        </a>
        <a href="">
          <img
            class="header__profile"
            src="../../assets/header/icon-profile.svg"
          />
        </a>
      </div>
    </div>
    <div class="header__bottom">
      <div class="header__items">
        <a
          class="header__item"
          v-for="(item, index) of headerItems"
          :key="index"
          :href="item.path"
          >{{ item.name }}</a
        >
      </div>
    </div>
  </header>
</template>

<script setup>
const headerItems = [
  {
    name: 'Plant pots',
    path: '/plant-pots',
  },
  {
    name: 'Ceramics',
    path: '/ceramics',
  },
  {
    name: 'Tables',
    path: '/tables',
  },
  {
    name: 'Chairs',
    path: '/chairs',
  },
  {
    name: 'Crockery',
    path: '/crockery',
  },
  {
    name: 'Tableware',
    path: '/tableware',
  },
  {
    name: 'Cutlery',
    path: '/cutlery',
  },
];
</script>

<style lang="scss" scoped>
@import url('https://fonts.cdnfonts.com/css/clash-display');

.header {
  background-color: #fff;
  height: 132px;
  margin: 0 30px;

  &__top {
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  }

  &__search {
    width: 20px;
    height: 20px;
  }

  &__title {
    font-family: 'Clash Display', sans-serif;
    font-size: 24px;
    line-height: 30px;
    color: #22202e;
    text-decoration: none;
  }

  &__menu--left,
  &__menu--right {
    display: flex;
    column-gap: 16px;
    flex: 0 1 50%;
  }

  &__menu--right {
    justify-content: flex-end;
  }

  &__cart {
    width: 20px;
    height: 20px;
  }

  &__profile {
    width: 20px;
    height: 20px;
  }

  &__bottom {
    height: 62px;
  }

  &__items {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    column-gap: 44px;
  }

  &__item {
    font-size: 16px;
    line-height: 22px;
    color: #726e8d;
    text-decoration: none;
  }
}
</style>
