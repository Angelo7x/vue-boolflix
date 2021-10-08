<template>
  <div class="card">
      <h2>{{attr.title ? attr.title : attr.name}}</h2>
      <h2>{{attr.original_title ? attr.original_title : attr.original_name}}</h2>
      <h2>{{attr.original_language}}</h2>
      <h2>{{attr.vote_average}}</h2>
      <img :src="`https://image.tmdb.org/t/p/w342/${attr.poster_path}`" alt="copertina">
  </div>
</template>

<script>
export default {
    name: 'Card',
    props: ['attr'],
}

</script>

<style lang="scss" scoped>
.card {
  display: flex;
  h2 {
    padding: 10px;
  }

}
</style>