<template>
  <button
  class="add"
  :class="isDark ? `add--dark`: ``"
  @click="onButtonAdd()"
  >Добавить книгу</button>
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
    onButtonAdd() {
      this.$emit('open-form');
    },
  },
  emits: ['open-form'],
};
</script>

<style lang="scss">
.add {
  border: none;
  background: none;
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 2rem;
  font-weight: 300;
  cursor: pointer;
  color: #F4F1DE;
  transition: color 0.3s;
  max-width: 200px;
  width: 100%;
  display: block;
  margin: 0 auto;
  padding: 10px 20px;
  margin-top: 30px;
  margin-bottom: 30px;
  background-color: #E07A5F;
  border-radius: 30px;

  &--dark {
    background-color: #3D405B;
  }
}
</style>
