<template>
  <div class="subscribe-form">
    <input
      class="subscribe-form__input"
      placeholder="your@email.com"
      :style="{ background: inputBackground, color: inputColor }"
    />
    <Button
      class="subscribe-form__btn"
      :color="buttonColor"
      >Sign up</Button
    >
  </div>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';

const props = defineProps({
  buttonColor: {
    type: String,
    default: 'primary',
  },
  inputColor: {
    type: String,
    required: false,
  },
  inputBackground: {
    type: String,
    required: false,
  },
});
</script>

<style lang="scss" scoped>
.subscribe-form {
  display: flex;
  height: 56px;

  &__input {
    width: 100%;
    background: rgba(255, 255, 255, 0.15);
    border: none;
    font-family: 'Satoshi', sans-serif;
    padding: 25px;
  }

  &__input::placeholder {
    font-size: 16px;
    line-height: 22px;
    font-weight: 300;
    @media (max-width: 480px) {
      font-size: 14px;
    }
  }

  &__btn {
    flex: 0 0 120px;
  }
}
</style>
