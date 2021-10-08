<template>
  <div class="card">
      <h2>{{attr.title ? attr.title : attr.name}}</h2>
      <h3>{{attr.original_title ? attr.original_title : attr.original_name}}</h3>
      <h4>{{attr.original_language}}</h4>
      <h5>{{attr.vote_average}}</h5>
      <img :src="`https://image.tmdb.org/t/p/w185/${attr.poster_path}`" alt="copertina">
  </div>
</template>

<script>
export default {
    name: 'Card',
    props: ['attr']
}
</script>

<style>

</style>