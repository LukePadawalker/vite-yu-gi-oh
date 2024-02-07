<script>
import { stringifyStyle } from '@vue/shared';
import { store } from '/src/data/store.js';
export default {
    name: 'PokemonCard',
    data: () => ({ store }),
    props: {
        number: Number,
        name: String,
        type1: String,
        image: String,
    }

}
</script>

<template>
    <div class="card">
        <img :src="image" alt="">
        <p>{{ number }}</p>
        <p>{{ name }}</p>
        <p>{{ type1 }}</p>
        <div class="element">
        </div>
    </div>
</template>

<style scoped>
img {
    max-width: 50px;
}

.card {
    width: calc(100% / 5 - 10px);
    height: calc(100% / 2 - 10px);
    background-color: aquamarine;
    border-radius: 20px;
}
</style>
