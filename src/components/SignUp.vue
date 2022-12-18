<template>
  <div class="sign-up">
    <div class="sign-up__container">
      <div class="sign-up__content">
        <h3 class="sign-up__title">Join the club and get the benefits</h3>
        <p class="sign-up__description">
          Sign up for our newsletter and receive exclusive offers on new ranges,
          sales, pop up stores and more
        </p>
        <SubscribeForm
          class="sign-up__form"
          input-background="#f9f9f9"
          button-color="primary-dark"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import SubscribeForm from '@/components/SubscribeForm.vue';
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.sign-up {
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 480px;
  background: #f9f9f9;

  &__container {
    width: 100%;
    background: #fff;
    margin: 60px 80px;
    display: flex;
    justify-content: center;
    @media (max-width: 1024px) {
      margin: 30px 40px;
    }
    @media (max-width: 480px) {
      margin: 0;
    }
  }

  &__content {
    max-width: 570px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 60px 30px;
    @media (max-width: 480px) {
      margin: 40px 20px 60px;
    }
  }

  &__title {
    font-family: $clash-display;
    font-weight: 400;
    font-size: 36px;
    line-height: 140%;
    text-align: center;
    color: $primary-dark;
    margin: 0 0 15px 0;
    @media (max-width: 480px) {
      font-size: 20px;
    }
  }

  &__description {
    max-width: 470px;
    font-size: 16px;
    line-height: 150%;
    text-align: center;
    color: $primary-dark;
    margin: 0 0 70px 0;
    @media (max-width: 480px) {
      font-size: 14px;
      margin: 0 0 35px 0;
    }
  }

  &__form {
    display: flex;
    width: 100%;
    max-height: 50px;
    padding: 0 50px;
    box-sizing: border-box;
    @media (max-width: 480px) {
      padding: 0;
    }
  }
}
</style>
