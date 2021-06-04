<template>
  <div
  class="book-card"
  :class="isDark ? `book-card--dark`: ``"
  >
    <img src="https://picsum.photos/seed/picsum/300/300" alt="" class="book-card__img" width="300" height="200">
    <h3 class="book-card__name">{{ book.name }}</h3>
    <ul class="book-card__genres">
      <li
      class="book-card__genre"
      v-for="genre in book.genres"
      v-bind:key="`${book.id}${genre}`"
      >
        {{genre}}
      </li>
    </ul>
    <ul class="book-card__authors">
      <li
      class="book-card__author"
      v-for="author in book.authors"
      v-bind:key="`${book.id}${author}`"
      >
        {{author}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Book',
  props: {
    book: {
      type: Object,
    },
    isDark: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss">
.book-card {
  max-width: 300px;
  min-height: 200px;
  background-color: #F2CC8F;
  border-radius: 20px;
  padding-bottom: 20px;
  transition: transform 0.3s;
  margin-top: 20px;
  transition: background-color 0.3s;

  &--dark {
    background-color: #3D405B;

    .book-card__name,
    .book-card__genres,
    .book-card__authors {
      color: #F4F1DE;
    }
  }

  &:hover {
    transform: scale(1.1);
  }
}

.book-card__img {
  object-fit: cover;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}

.book-card__name,
.book-card__genres,
.book-card__authors {
  padding-left: 20px;
  padding-right: 20px;
  color: #3D405B;
  transition: color 0.3s;
}

.book-card__name {
  font-size: 2rem;
  margin-top: 10px;
}

.book-card__genres {
  font-size: 1.5rem;
  margin-top: 10px;
}

.book-card__authors {
  font-size: 1.8rem;
  margin-top: 10px;
}

.book-card__genres,
.book-card__authors {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  margin-left: -10px;
}

.book-card__genre,
.book-card__author {
  margin-left: 10px;
}
</style>
