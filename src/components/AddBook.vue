<template>
  <button
  class="theme-switcher"
  :class="isDark ? `theme-switcher--dark`: ``"
  @click="onThemeChange()"
  >Сменить тему</button>
</template>

<script>
export default {
  name: 'ThemeSwitcher',
  props: {
    isDark: {
      type: Boolean,
    },
  },
  methods: {
    onThemeChange() {
      this.$emit('change-theme');
    },
  },
  emits: ['change-theme'],
};
</script>

<style lang="scss">
.theme-switcher {
  border: none;
  background: none;
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 2rem;
  font-weight: 300;
  cursor: pointer;
  color: #3D405B;
  transition: color 0.3s;

  &--dark {
    color: #F4F1DE;
  }
}
</style>
