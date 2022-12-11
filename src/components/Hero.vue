<template>
  <div class="hero">
    <div class="hero__info">
      <h1 class="hero__title">
        Luxury homeware for people who love timeless design quality
      </h1>
      <p class="hero__description">
        With our new collection, view over 400 bespoke pieces from homeware
        through to furniture today
      </p>
      <a
        href="#"
        class="hero__link"
        >View collection</a
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.hero {
  background: url('../../public/hero/hero.jpg') no-repeat top center;
  background-size: cover;
  max-height: 704px;
  display: flex;
  align-items: center;

  &__info {
    background: #fff;
    width: 630px;
    height: 444px;
    padding: 48px 61px 46px 56px;
    display: flex;
    flex-direction: column;
    margin: 130px 80px 130px auto;
  }

  &__title {
    font-family: 'Clash Display', sans-serif;
    font-size: 32px;
    font-weight: 400;
    line-height: 140%;
    color: #22202e;
    margin: 0 0 20px 0;
  }

  &__description {
    font-family: 'Satoshi', sans-serif;
    font-size: 18px;
    line-height: 150%;
    color: #5b5676;
  }

  &__link {
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
    line-height: 150%;
    color: #2a254b;
    padding: 16px 32px;
    text-decoration: none;
    background: #f9f9f9;
    align-self: baseline;
    margin-top: auto;
  }
}
</style>
