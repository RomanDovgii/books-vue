<template>
  <main
  class="main"
  :class="isDark ? `main--dark`: ``"
  >
    <Selectors @select-genre="changeGenreBridgeMain"
    :genres="genres"
    :selectedGenre="selectedGenre"/>
    <Books :books="books" :isDark="isDark"/>
    <AddBook
    @open-form="openFormBridge"
    :isDark="isDark"/>
  </main>
</template>

<script>
import Selectors from './Selectors.vue';
import Books from './Books.vue';
import AddBook from './AddBook.vue';

export default {
  name: 'Main',
  components: {
    Selectors,
    Books,
    AddBook,
  },
  props: {
    books: {
      type: Array,
    },
    genres: {
      type: Array,
    },
    isDark: {
      type: Boolean,
    },
    selectedGenre: {
      type: String,
    },
  },
  methods: {
    changeGenreBridgeMain(genre) {
      this.$emit('select-genre', genre);
    },
    openFormBridge() {
      this.$emit('open-form');
    },
  },
};
</script>

<style lang="scss">
.main {
  flex-grow: 1;
  background-color: #F4F1DE;
  transition: background-color 0.3s;

  &--dark {
    background-color: #313131f6;
  }
}
</style>
