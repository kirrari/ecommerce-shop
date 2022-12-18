<template>
  <div class="sign-up">
    <div class="sign-up__container">
      <div class="sign-up__content">
        <h3 class="sign-up__title">Join the club and get the benefits</h3>
        <p class="sign-up__description">
          Sign up for our newsletter and receive exclusive offers on new ranges,
          sales, pop up stores and more
        </p>
        <form class="sign-up__form">
          <input
            type="text"
            class="sign-up__input"
            placeholder="your@email.com"
          />
          <Button
            path="/"
            class="sign-up__btn"
            color="primary-dark"
            >Sign up</Button
          >
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';

console.log(Button);
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
  }

  &__content {
    max-width: 570px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 60px auto;
  }

  &__title {
    font-family: $clash-display;
    font-weight: 400;
    font-size: 36px;
    line-height: 140%;
    text-align: center;
    color: $primary-dark;
    margin: 0 0 15px 0;
  }

  &__description {
    max-width: 470px;
    font-size: 16px;
    line-height: 150%;
    text-align: center;
    color: $primary-dark;
    margin: 0 0 70px 0;
  }

  &__form {
    display: flex;
    width: 100%;
    max-height: 50px;
    padding: 0 50px;
    box-sizing: border-box;
  }

  &__input {
    background: #f9f9f9;
    border: none;
    width: 100%;
    &::placeholder {
      color: #d9d9d9;
      padding: 0 30px;
      font-size: 16px;
      line-height: 22px;
      font-family: $satoshi;
    }
  }

  &__btn {
    width: 140px;
  }
}
</style>
