<template>
  <div class="hero">
    <InfoBlock
      class="hero__info"
      title="Luxury homeware for people who love timeless design quality"
      description="With our new collection, view over 400 bespoke pieces from homeware
        through to furniture today"
      link="View collection"
      title-color="#22202E"
      button-color="secondary"
      background-color="#fff"
    />
    <img
      class="hero__img"
      src="/hero/hero-mobile.jpg"
      alt=""
    />
  </div>
</template>

<script setup>
import InfoBlock from '@/components/InfoBlock.vue';
</script>

<style lang="scss" scoped>
.hero {
  background: url('/hero/hero.jpg') no-repeat top center;
  background-size: cover;
  max-height: 704px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  &__info {
    box-sizing: border-box;
    max-width: 630px;
    padding: 50px;
    display: flex;
    flex-direction: column;
    margin: 130px 80px 130px auto;
    @media (max-width: 1024px) {
      margin: 60px 40px;
    }
    @media (max-width: 480px) {
      margin: 0;
      padding: 30px 20px;
    }
  }

  &__img {
    object-fit: cover;
    @media (min-width: 481px) {
      display: none;
    }
  }
}
</style>
