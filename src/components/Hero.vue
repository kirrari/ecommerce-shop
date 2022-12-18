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
  align-items: center;

  &__info {
    box-sizing: border-box;
    background: #fff;
    width: 630px;
    height: 444px;
    padding: 48px 61px 46px 56px;
    display: flex;
    flex-direction: column;
    margin: 130px 80px 130px auto;
  }
}
</style>
