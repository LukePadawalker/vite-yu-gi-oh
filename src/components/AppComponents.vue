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
    <div>
        <AppPokemonCard v-for="pokemon in pokemons" />
    </div>
</template>

<style scoped></style>
