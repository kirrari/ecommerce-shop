<template>
  <header class="header">
    <div class="header__top">
      <div class="header__menu--left">
        <a href="">
          <img
            class="header__search"
            src="/header/icon-search.svg"
          />
        </a>
      </div>
      <router-link
        to="/"
        class="header__title"
        >Avion</router-link
      >
      <div class="header__menu--right">
        <router-link to="/cart">
          <img
            class="header__cart"
            src="/header/icon-cart.svg"
            alt="Cart"
          />
        </router-link>
        <router-link to="/profile">
          <img
            class="header__profile"
            src="/header/icon-profile.svg"
            alt="Profile"
          />
        </router-link>
      </div>
    </div>
    <div class="header__bottom">
      <div class="header__items">
        <router-link
          :to="item.path"
          class="header__item"
          v-for="(item, index) of headerItems"
          :key="index"
          >{{ item.name }}</router-link
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
@import '@/assets/styles/variables.scss';

.header {
  background-color: #fff;
  margin: 0 30px;

  @media (max-width: 480px) {
    margin: 0 20px;
  }

  &__top {
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    @media (max-width: 767px) {
      flex-direction: row-reverse;
      justify-content: space-between;
    }
  }

  &__search {
    width: 20px;
    height: 20px;
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
  }

  &__title {
    font-family: $clash-display;
    font-size: 24px;
    line-height: 30px;
    color: $secondary-dark;
    text-decoration: none;
  }

  &__menu--left,
  &__menu--right {
    display: flex;
    column-gap: 16px;
    flex: 0 1 50%;
  }

  &__menu--left {
    @media (max-width: 767px) {
      justify-content: flex-end;
    }
  }

  &__menu--right {
    justify-content: flex-end;
    @media (max-width: 767px) {
      display: none;
    }
  }

  &__cart {
    width: 20px;
    height: 20px;
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
    @media (max-width: 767px) {
      display: none;
    }
  }

  &__profile {
    width: 20px;
    height: 20px;
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
    @media (max-width: 767px) {
      display: none;
    }
  }

  &__bottom {
    height: 62px;
    @media (max-width: 767px) {
      display: none;
    }
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
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
  }
}
</style>
