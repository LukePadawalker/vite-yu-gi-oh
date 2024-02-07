<script>
import axios from 'axios'
import { store } from './data/store.js';
import AppMain from './components/AppMain.vue';
import { apiUri } from '/src/data/';
import { colorMap } from '/src/data/';

const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc';
export default {

  name: 'Pokemonlist',
  components: { AppMain },
  methods: {
    async fetchPokemon(endpoint = apiUri) {
      axios.get(endpoint).then(res => {
        store.pokemons = res.data.docs;
      })
    },
    async fetchTypes(endpoint = colorMap) {
      axios.get(endpoint).then(res => {
        store.types = res.data;
      })
    },

  },
  created() {
    this.fetchPokemon();
    this.fetchTypes();
  }
}
</script>

<template>
  <div>
    <AppMain @read-value="" />
  </div>
</template>

<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
