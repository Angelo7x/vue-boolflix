<template>
  <div class="films-container">
      <ul>
          <li v-for="(film, index) in elems" :key="index">
              <Card :attr="film"/>
          </li>
      </ul>

      <ul>
          <li v-for="(serie, index) in serie" :key="index">
              <Card :attr="serie"/>
          </li>
      </ul>
    
  </div>
</template>

<script>
import Card from "./Card.vue"
export default {
    name: 'Films',
    props: ['elems', 'serie'],
    components: {
        Card
    }
}
</script>

<style>

</style>