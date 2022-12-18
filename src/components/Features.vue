<template>
  <div class="features">
    <InfoBlock
      class="features__info"
      title="It started with a small idea"
      description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
      link="View collection"
      title-color="#fff"
      description-color="#fff"
      background-color="#2a254b"
      button-color="primary"
    />
    <img
      class="features__img"
      src="/features/features1.jpg"
      alt="Feature"
    />
  </div>
</template>

<script setup>
import InfoBlock from '@/components/InfoBlock.vue';
</script>

<style lang="scss" scoped>
.features {
  display: flex;
  column-gap: 12px;
  margin: 60px 80px;

  &__info {
    box-sizing: border-box;
    width: 634px;
    height: 478px;
    padding: 65px 75px 55px 65px;
  }

  &__img {
    width: 634px;
    height: 478px;
  }
}
</style>
