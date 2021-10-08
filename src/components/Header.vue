<template>
  <header>
      <div class="title">
            <h1>Boolflix</h1>
      </div>
      <div class="inputs">
            <input class="text" type="text" placeholder="Inserisci il nome del film" v-model="searchInp">
            <button class="btn" @click="$emit('search', searchInp)">Cerca</button>
      </div>
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

<style lang="scss" scoped>
header {
    height: 100px;
    background-color: black;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    .inputs {
        .text {
            padding: 4px 20px;
            border-radius: 10px;
        }
        .btn {
            margin-left: 20px;
            padding: 4px 10px;
            border-radius: 10px;
        }
    }
    .title {
        color: red
    }
}

</style>