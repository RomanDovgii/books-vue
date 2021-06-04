<template>
  <section class="books">
    <div class="books__wr">
      <h2 class="books__heading" id="books">Книги:</h2>
      <ul class="books__list">
        <li
        class="books__el"
        v-for="book in books"
        :key="`${book.id}${book.name}${book.genres[0]}`"
        >
          <Book :book="book" :isDark="isDark"/>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import Book from './Book.vue';

export default {
  name: 'Books',
  components: {
    Book,
  },
  props: {
    books: {
      type: Array,
    },
    isDark: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss">
.books {
  padding-top: 20px;
  padding-bottom: 20px;
}

.books__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  flex-direction: column;
  padding-right: 30px;
  padding-left: 30px;
  margin: 0 auto;
}

.books__heading {
  font-size: 3rem;
  color: #E07A5F;
  font-weight: 300;
}

.books__list {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  justify-content: space-between;
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
}

@media (max-width: 360px) {
  .books__wr {
    padding-left: 5px;
    padding-right: 5px;
    align-items: center;
  }

  .books__list {
    justify-content: center;
  }
}
</style>
