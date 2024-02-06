<script>
import axios from 'axios'
import { store } from '/src/store.js';
import AppMain from './components/AppMain.vue';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
export default {
  name: 'pokemonlist',
  created() {
    axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
      console.log(store.pokemons)
    })
  }
}
</script>

<template>
  <div>
    <AppMain />

  </div>
</template>

<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
