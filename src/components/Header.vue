<template>
  <header>
      <input type="text" placeholder="Inserisci il nome del film" v-model="searchInp">
      <button @click="$emit('search', searchInp)">Cerca</button>
  </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            searchInp: ""
        }
    }
}
</script>

<style>

</style>