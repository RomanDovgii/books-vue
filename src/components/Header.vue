<template>
  <header
  class="header"
  :class="isDark ? `header--dark`: ``">
    <div class="header__wr">
      <Logo :isDark="isDark"/>
      <ThemeSwitcher @change-theme="changeTheme" :isDark="isDark"/>
    </div>
  </header>
</template>

<script>
import Logo from './Logo.vue';
import ThemeSwitcher from './ThemeSwitcher.vue';

export default {
  name: 'Header',
  props: {
    isDark: {
      type: Boolean,
    },
  },
  components: {
    Logo,
    ThemeSwitcher,
  },
  methods: {
    changeTheme() {
      this.$emit('change-theme');
    },
  },
  emits: ['change-theme'],
};
</script>

<style lang="scss">
.header {
  transition: background-color 0.3s;
  background-color: #F2CC8F;

  min-height: 50px;

  &--dark {
    background-color: #3D405B;
  }
}

.header__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-right: 30px;
  padding-left: 30px;
  margin: 0 auto;
}
</style>
