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
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px 16px;
  margin: 60px 80px;
  @media (max-width: 1024px) {
    grid-template-columns: 1fr;
    margin: 30px 40px;
  }
  @media (max-width: 480px) {
    margin: 30px 20px;
  }

  &__info {
    box-sizing: border-box;
    padding: 65px 75px 55px 65px;
    @media (max-width: 480px) {
      padding: 30px;
    }
  }

  &__img {
    height: 100%;
    object-fit: cover;
  }
}
</style>
