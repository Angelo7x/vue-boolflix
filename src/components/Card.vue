<template>
  <div class="card">
      <h2>{{attr.title}}</h2>
      <h3>{{attr.original_title}}</h3>
      <h4>{{attr.original_language}}</h4>
      <h5>{{attr.vote_average}}</h5>
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