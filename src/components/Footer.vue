<template>
  <footer
  class="footer"
  :class="isDark ? `footer--dark`: ``"
  >
    <div class="footer__wr">
      <Developer :isDark="isDark"/>
      <Logo :isDark="isDark"/>
    </div>
  </footer>
</template>

<script>
import Logo from './Logo.vue';
import Developer from './Developer.vue';

export default {
  name: 'Footer',
  props: {
    isDark: {
      type: Boolean,
    },
  },
  components: {
    Logo,
    Developer,
  },
};
</script>

<style lang="scss">
.footer {
  background-color: #F2CC8F;

  display: flex;
  justify-content: center;

  min-height: 50px;

  &--dark {
    background-color: #3D405B;
  }
}

.footer__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding-right: 30px;
  padding-left: 30px;
}
</style>
