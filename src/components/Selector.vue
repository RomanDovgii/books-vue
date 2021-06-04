<template>
  <button
  class="selector"
  :class="selectedGenre === genre ? 'selector--selected' : ''"
  >{{genre}}</button>
</template>

<script>
export default {
  name: 'Selector',
  props: {
    genre: {
      type: String,
    },
    selectedGenre: {
      type: String,
    },
  },
};
</script>

<style lang="scss">
.selector {
  border: none;
  background: none;
  align-self: flex-start;
  font-size: 3rem;
  color: #F4F1DE;
  font-weight: 300;
  margin-left: 10px;
  font-family: 'Open Sans Condensed', sans-serif;
}

.selector--selected {
  font-weight: 700;
}
</style>
