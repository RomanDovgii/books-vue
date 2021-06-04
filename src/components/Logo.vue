<template>
  <a class="logo">
    <p
    class="logo__heading"
    :class="isDark ? `logo__heading--dark`: ``"
    >Мои Книги</p>
  </a>
</template>

<script>
export default {
  name: 'Logo',
  props: {
    isDark: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss">
.logo {
  display: flex;
  align-items: center;
}

.logo__heading {
  color: #3D405B;
  font-size: 4rem;
  padding-top: 20px;
  padding-bottom: 20px;
  font-weight: 700;
  transition: color 0.3s;

  &--dark {
    color: #F4F1DE;
  }
}
</style>
