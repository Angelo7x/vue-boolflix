<template>
  <div class="card-container">
      <img class="card-poster" :src="`https://image.tmdb.org/t/p/w342/${attr.poster_path}`" alt="poster">
    <div class="card-info">
      <h2>Titolo : {{attr.title ? attr.title : attr.name}}</h2>
      <h2 class="opacity">Titolo originale : {{attr.original_title ? attr.original_title : attr.original_name}}</h2>
      <h2>Lingua originale : {{attr.original_language}}</h2>
      <h2>Voto : {{attr.vote_average}}</h2>
      <h2 class="overview opacity">Overview : {{attr.overview}}</h2>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Card',
    props: ['attr'],
}

</script>

<style lang="scss" scoped>
.card-container {
  position: relative;
  color: white;

  &:hover .card-info {
    opacity: 1;
  }

  .card-info {
    position: absolute;
    top: 0;
    left: 50%;
    opacity: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    width: 30%;
    height: 100%;
    overflow-y: scroll;
    h2 {
      padding: 20px;
    }

    .opacity {
      opacity: 0.6;
    }

  }
}
</style>