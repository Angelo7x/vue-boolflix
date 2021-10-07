<template>
  <div id="app">
    <Header @search="searchFilm"/>
    <Films/>
  </div>
</template>

<script>
// import axios from 'axios';
import Header from "./components/Header.vue";
import Films from "./components/Films";

export default {
  name: 'App',
  components: {
    Header,
    Films,
  },
  methods: {
    searchFilm(text) {
      console.log(text);
    }
  }
}
</script>

<style lang="scss">

</style>
