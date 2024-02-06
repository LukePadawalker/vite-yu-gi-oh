<script>
import { store } from '/src/store.js';
import AppPokemonCard from './AppPokemonCard.vue'
export default {
    name: 'AppComponents',
    pokemons: store.pokemons,
    data: () => ({ store })

}
</script>

<template>
    <div>
        <AppPokemonCard />
    </div>
</template>

<style scoped></style>
