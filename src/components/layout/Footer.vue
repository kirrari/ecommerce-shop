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
          <SubscribeForm
            class="footer__form"
            button-color="secondary"
            input-color="#fff"
          />
        </div>
      </div>
      <div class="footer__bottom">
        <span class="footer__copyright">Copyright 2022 Avion LTD</span>
        <div class="footer__icons">
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-linkedin.svg"
          /></a>
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-facebook.svg"
          /></a>
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-instagram.svg"
          /></a>
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-skype.svg"
          /></a>
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-twitter.svg"
          /></a>
          <a
            href="#"
            class="footer__icon"
            ><img src="footer/icon-pinterest.svg"
          /></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import SubscribeForm from '@/components/SubscribeForm.vue';
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.footer {
  color: #fff;
  background: $primary-dark;

  &__container {
    padding: 60px 80px 0;
    @media (max-width: 1024px) {
      padding: 30px 40px 0;
    }
    @media (max-width: 480px) {
      padding: 30px 20px 0;
    }
  }

  &__top {
    display: flex;
    padding: 0 0 50px 0;
    border-bottom: 1px solid #4e4d93;
    column-gap: 60px;

    @media (max-width: 1024px) {
      flex-direction: column;
    }
  }

  &__content {
    display: flex;
    flex: 1 0 440px;
    gap: 80px;

    @media (max-width: 1024px) {
      flex: 1 0 100%;
      margin: 0 0 50px 0;
    }
    @media (max-width: 480px) {
      flex-wrap: wrap;
      gap: 40px 100px;
      margin: 0 0 40px 0;
    }
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
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
  }

  &__subscribe {
    flex: 0 1 50%;
  }

  &__title--subscribe {
    display: block;
    margin: 0 0 15px 0;
  }

  &__btn {
    width: 140px;
  }

  &__bottom {
    display: flex;
    padding: 20px 0;
    justify-content: space-between;
    @media (max-width: 480px) {
      flex-direction: column;
      align-items: center;
      row-gap: 20px;
    }
  }

  &__copyright {
    font-size: 14px;
    line-height: 19px;
  }

  &__icons {
    display: flex;
    column-gap: 24px;
  }

  &__icon {
    transition: all 0.3s ease;
    &:hover {
      opacity: 0.7;
    }
  }
}
</style>
