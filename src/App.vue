<template>
  <Header/>
  <Main/>
  <Footer/>
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
    };
  },
  created() {
    this.books = [
      {
        name: 'Преступление и наказание',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
      {
        name: '',
        genres: [
          '',
          '',
        ],
        Authors: [
          '',
          '',
        ],
        description: '',
      },
    ];
  },
};
</script>

<style lang="scss">
html {
  font-size: 62.5%;
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
