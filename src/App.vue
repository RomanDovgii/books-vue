<template>
  <h1 class="visually-hidden">Мои книги</h1>
  <Header :isDark="this.state.isDark" @change-theme="changeTheme"/>
  <Main
  :isDark="this.state.isDark"
  :selectedGenre="this.state.selectedGenre"
  :books="books"
  :genres="genres"/>
  <Footer :isDark="this.state.isDark"/>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      books: [],
      state: {},
    };
  },
  created() {
    this.books = [
      {
        id: 1,
        name: 'Преступление и наказание',
        genres: [
          'Роман',
          'Драма',
        ],
        authors: [
          'Федор Достоевский',
        ],
        description: 'lorem ipsum',
      },
      {
        id: 2,
        name: 'Преступление и наказание',
        genres: [
          'Фэнтези',
          'Лингвистика',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 3,
        name: 'Преступление и наказание',
        genres: [
          'Сказки',
          'Рассказы',
        ],
        authors: [
          'Паша',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 4,
        name: 'Преступление и наказание',
        genres: [
          'Мифы древней Греции',
          'Веселые истории',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 5,
        name: 'Преступление и наказание',
        genres: [
          'Анекдоты',
          'Бред',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 6,
        name: 'Преступление и наказание',
        genres: [
          'Религии',
          'Бред',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 7,
        name: 'Преступление и наказание',
        genres: [
          'Психология',
          'Философия',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 8,
        name: 'Преступление и наказание',
        genres: [
          'Программирование',
          'Бред',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 9,
        name: 'Преступление и наказание',
        genres: [
          'Истории',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 10,
        name: 'Преступление и наказание',
        genres: [
          'Скучное',
          'Учебники',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 11,
        name: 'Преступление и наказание',
        genres: [
          'Сети',
          'Cisco',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
      {
        id: 12,
        name: 'Преступление и наказание',
        genres: [
          'Документации',
          'Vue',
        ],
        authors: [
          'Женя',
          'Ваня',
        ],
        description: 'Преступление и наказание',
      },
    ];
    this.state = {
      isDark: false,
      selectedGenre: 'Всё',
    };
    this.genres = this.sortGenres(this.books);
  },
  methods: {
    changeTheme() {
      this.state.isDark = !this.state.isDark;
    },
    sortGenres(books) {
      if (books.length !== 0) {
        const genres = books.reduce((accumulator, book) => {
          book.genres.forEach((genre) => {
            if (!accumulator.includes(genre)) {
              accumulator.push(genre);
            }
          });

          return accumulator;
        }, []);
        return ['Всё', ...genres];
      }
      return [];
    },
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@300;700&display=swap');

html {
  font-size: 62.5%;
  font-family: 'Open Sans Condensed', sans-serif;
}

*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body #app{
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    margin: -1px;
    border: 0;
    padding: 0;

    white-space: nowrap;
    clip-path: inset(100%);
    clip: rect(0 0 0 0);
    overflow: hidden;
  }
</style>
