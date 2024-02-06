<script>
import { store } from '/src/store.js';
import AppPokemonCard from './AppPokemonCard.vue'
export default {
    components: { AppPokemonCard },
    name: 'AppComponents',
    pokemons: store.pokemons,
    data: () => ({ store })

}
</script>

<template>
    <div id="root">
        <AppPokemonCard v-for="pokemon in pokemons" />
    </div>
</template>

<style scoped>
#root {
    width: 95%;
    height: 83%;
    background-color: rgb(73, 72, 72);
    border: 10px solid transparent;
    display: flex;
    gap: 5px;

}
</style>
