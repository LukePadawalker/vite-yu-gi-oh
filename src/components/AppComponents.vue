<script>
import { store } from '/src/store.js';
import AppPokemonCard from './AppPokemonCard.vue'
export default {
    components: { AppPokemonCard },
    name: 'AppComponents',
    data: () => ({ store })

}
</script>

<template>
    <div id="root">
        <AppPokemonCard v-for="pokemon in store.pokemons" v-bind="pokemon" />
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
