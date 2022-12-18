<template>
  <div
    class="info"
    :style="{ background: backgroundColor }"
  >
    <h1
      class="info__title"
      :style="{ color: titleColor }"
    >
      {{ title }}
    </h1>
    <p
      class="info__description"
      :style="{ color: descriptionColor }"
    >
      {{ description }}
    </p>
    <Button
      type="link"
      path="/"
      class="info__link"
      :color="buttonColor"
      >View collection</Button
    >
  </div>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  link: {
    type: String,
    required: true,
  },
  titleColor: {
    type: String,
    default: '#22202E',
  },
  descriptionColor: {
    type: String,
    default: '#5b5676',
  },
  backgroundColor: {
    type: String,
    default: '#fff',
  },
  buttonColor: {
    type: String,
    default: 'primary',
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.info {
  background: #fff;
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  &__title {
    font-family: $clash-display;
    font-size: 32px;
    font-weight: 400;
    line-height: 140%;
    color: $secondary-dark;
    margin: 0 0 20px 0;
  }

  &__description {
    font-size: 18px;
    line-height: 150%;
    color: #5b5676;
  }

  &__link {
    font-size: 16px;
    line-height: 150%;
    padding: 16px 32px;
    text-decoration: none;
    align-self: baseline;
    margin-top: auto;
  }
}
</style>
