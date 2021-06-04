<template>
  <main class="main">
    <Selectors/>
    <Books :books="books"/>
  </main>
</template>

<script>
import Selectors from './Selectors.vue';
import Books from './Books.vue';

export default {
  name: 'Main',
  components: {
    Selectors,
    Books,
  },
  props: {
    books: {
      type: Array,
    },
  },
};
</script>

<style lang="scss">
.main {
  flex-grow: 1;
  background-color: #F4F1DE;
}
</style>
