<script>
import axios from 'axios'
import { store } from './store.js';
import AppMain from './components/AppMain.vue';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
export default {

  name: 'Pokemonlist',
  components: { AppMain },
  methods: {
    async fetchPokemon() {
      await axios.get(endpoint).then(res => {
        const pokemons = res.data.pokemons;
        console.log(pokemons)
        store.pokemons = pokemons.map(pokemon => {
          const { name, number, type1, imageUrl } = pokemon;
          return { name, number, mainType: type1, imageUrl }
        })
      })
    }
  },
  created() {
    this.fetchPokemon();
  },
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
