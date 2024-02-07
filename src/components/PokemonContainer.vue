<script>
import { store } from '/src/data/store.js';
import PokemonCard from './PokemonCard.vue'
export default {
    components: { PokemonCard },
    name: 'PokemonContainer',
    data: () => ({ store }),

}
</script>

<template>
    <div id="root">
        <PokemonCard v-for="pokemon in store.pokemons" :number="pokemon.number" :image="pokemon.imageUrl"
            :name="pokemon.name" :type1="pokemon.type1" />

    </div>
</template>

<style scoped>
#root {
    width: 95%;
    height: 83%;
    background-color: rgb(73, 72, 72);
    border: 10px solid transparent;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    overflow: hidden;

}
</style>
