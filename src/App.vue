<script>
import axios from 'axios'
import { store } from './data/store.js';
import AppMain from './components/AppMain.vue';
import { apiUri } from '/src/data/';
import { colorMap } from '/src/data/';

export default {

  name: 'Pokemonlist',
  components: { AppMain },
  methods: {
    async fetchPokemon(endpoint = apiUri) {
      axios.get(endpoint).then(res => {
        store.pokemons = res.data.docs;
        console.log(store.pokemons)

      })
    },
    async fetchTypes(endpoint = colorMap) {
      axios.get(endpoint).then(res => {
        store.types = res.data;
      })
    },

    filteredPokemon(type) {
      const endpoint = type ? `${apiUri}?eq[type1]=${type}` : apiUri;
      this.fetchPokemon(endpoint)

    },
    created() {
      this.fetchPokemon();
      this.fetchTypes();
    }
  }
}
</script>

<template>
  <div>
    <AppMain @read-value="filteredPokemon" />
  </div>
</template>

<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
