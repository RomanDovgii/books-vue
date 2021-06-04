<template>
  <a class="logo" href="#books">
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
  text-decoration: none;
}

.logo__heading {
  color: #3D405B;
  font-size: 4rem;
  padding-top: 20px;
  padding-bottom: 20px;
  font-weight: 700;
  transition: color 0.3s;
  animation: move;
  animation-direction: normal;
  animation-duration: 0.5s;

  &--dark {
    color: #F4F1DE;
  }
}

@keyframes move {
  0% {
    opacity: 0;
    transform: translateX(-50px);
  }
  100% {
    opacity: 1;
    transform: translateX(0px);
  }
}
</style>
