<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__top">
        <div class="footer__content">
          <div class="footer__links">
            <span class="footer__title--link">Menu</span>
            <router-link
              class="footer__link"
              to="/"
              >New arrivals</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Best sellers</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Recently viewed</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Popular this week</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >All products</router-link
            >
          </div>
          <div class="footer__links">
            <span class="footer__title--link">Categories</span>
            <router-link
              class="footer__link"
              to="/"
              >Crockery</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Furniture</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Homeware</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Plant pots</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Chairs</router-link
            >
          </div>
          <div class="footer__links">
            <span class="footer__title--link">Our company</span>
            <router-link
              class="footer__link"
              to="/"
              >About us</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Vacancies</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Contact us</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Privacy</router-link
            >
            <router-link
              class="footer__link"
              to="/"
              >Returns policy</router-link
            >
          </div>
        </div>
        <div class="footer__subscribe">
          <span class="footer__title--subscribe">Join our mailing list</span>
          <div class="footer__form">
            <input
              class="footer__input"
              placeholder="your@email.com"
            />
            <Button
              class="footer__btn"
              color="secondary"
              >Sign up</Button
            >
          </div>
        </div>
      </div>
      <div class="footer__bottom">
        <span class="footer__copyright">Copyright 2022 Avion LTD</span>
        <div class="footer__icons">
          <img
            src=""
            class="footer__icon"
          />
          <img
            src=""
            class="footer__icon"
          />
          <img
            src=""
            class="footer__icon"
          />
          <img
            src=""
            class="footer__icon"
          />
          <img
            src=""
            class="footer__icon"
          />
          <img
            src=""
            class="footer__icon"
          />
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.footer {
  color: #fff;
  background: $primary-dark;

  &__container {
    padding: 60px 80px 0;
  }

  &__top {
    display: flex;
    padding: 0 0 50px 0;
    border-bottom: 1px solid #4e4d93;
  }

  &__content {
    display: flex;
    flex: 0 1 50%;
    column-gap: 120px;
  }

  &__links {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
  }

  &__title--link {
  }

  &__link {
    color: #fff;
    font-size: 14px;
    line-height: 20px;
    font-weight: 300;
  }

  &__subscribe {
    flex: 0 1 50%;
  }

  &__title--subscribe {
    display: block;
    margin: 0 0 15px 0;
  }

  &__form {
    display: flex;
  }

  &__input {
    width: 100%;
    background: rgba(255, 255, 255, 0.15);
    border: none;
  }

  &__input::placeholder {
    font-size: 16px;
    line-height: 22px;
    color: #ffffff84;
    padding: 30px;
    font-weight: 300;
  }

  &__btn {
    width: 140px;
  }

  &__bottom {
    display: flex;
    padding: 20px 0;
  }

  &__copyright {
    font-size: 14px;
    line-height: 19px;
  }

  &__icons {
  }

  &__icon {
  }
}
</style>
