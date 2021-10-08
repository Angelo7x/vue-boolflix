<template>
  <div id="app">
    <Header @search="searchFilm"/>
    <Films :elems="films" :serie="series"/>
  </div>
</template>

<script>
import axios from 'axios';
import Header from "./components/Header.vue";
import Films from "./components/Films";

export default {
  name: 'App',
  components: {
    Header,
    Films,
  },
  data() {
    return {
      films: [],
      series: []
    }
  },
  methods: {
    searchFilm(text) {
      axios.get('https://api.themoviedb.org/3/search/movie', {
        params: {
          api_key: 'ff6eb15fc7fa9fcec3445ca68a2bccee',
          query: text,
          language: 'it-IT',
        }
      })
      .then( (response) => {
        this.films = response.data.results;
      });

      axios.get('https://api.themoviedb.org/3/search/tv', {
        params: {
          api_key: 'ff6eb15fc7fa9fcec3445ca68a2bccee',
          query: text,
          language: 'it-IT',
        }
      })
      .then( (response) => {
        this.series = response.data.results;
      });
    }
  }
}
</script>

<style lang="scss">

</style>
