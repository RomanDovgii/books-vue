<template>
  <section class="selectors">
    <div class="selectors__wr">
      <h2 class="selectors__heading">Сортировка по жанрам:</h2>
      <ul class="selectors__list">
        <li class="selectors__el"
          v-for="genre in genres"
          v-bind:key="`${genre}-selector`"
        >
        <Selector
        @select-genre="changeGenreBridgeSelectors"
        :genre="genre"
        :selectedGenre="selectedGenre"/>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import Selector from './Selector.vue';

export default {
  name: 'Selectors',
  props: {
    genres: {
      type: Array,
    },
    selectedGenre: {
      type: String,
    },
  },
  components: {
    Selector,
  },
  methods: {
    changeGenreBridgeSelectors(genre) {
      this.$emit('select-genre', genre);
    },
  },
};
</script>

<style lang="scss">
.selectors {
  background-color: rgba(#E07A5F, 1.0);
  display: flex;
  justify-content: center;
  padding-top: 20px;
  padding-bottom: 20px;
}

.selectors__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  padding-right: 30px;
  padding-left: 30px;
}

.selectors__heading {
  font-size: 3rem;
  color: #F4F1DE;
  font-weight: 300;
  min-width: 250px;
}

.selectors__list {
  list-style: none;
  align-self: flex-end;
  display: flex;
  flex-wrap: wrap;
}
</style>
