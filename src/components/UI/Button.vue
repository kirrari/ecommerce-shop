<template>
  <button
    v-if="type === 'button'"
    :class="['btn', `btn--${color}`]"
  >
    <slot />
  </button>
  <router-link
    v-else
    :class="['btn', `btn--${color}`]"
    :to="path"
  >
    <slot />
  </router-link>
</template>

<script setup>
const props = defineProps({
  background: {
    type: String,
    required: false,
  },
  type: {
    type: String,
    default: 'button',
  },
  path: {
    type: String,
    default: '/',
  },
  color: {
    type: String,
    default: 'primary',
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';

.btn {
  font-family: 'Satoshi', sans-serif;
  border: none;
  font-size: 16px;
  padding: 16px 32px;
  display: inline-flex;
  justify-content: center;
  text-decoration: none;
  align-items: center;
  cursor: pointer;
  transition: all 0.3s;
  &:hover {
    opacity: 0.8;
  }
  &--primary {
    color: #fff;
    background: rgba(249, 249, 249, 0.15);
  }
  &--secondary {
    color: $secondary-dark;
    background: #f9f9f9;
  }
  &--primary-dark {
    color: #fff;
    background: $primary-dark;
  }
}
</style>
