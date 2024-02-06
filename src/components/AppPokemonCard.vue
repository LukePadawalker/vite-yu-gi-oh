<script>
import { stringifyStyle } from '@vue/shared';
import { store } from '/src/store.js';
export default {
    name: 'AppPokemonCard',
    data: () => ({ store }),
    props: {
        number: String,
        name: String,
        type1: String,
        img: String,
    }

}
</script>

<template>
    <div class="card">
        <img :src="img" alt="">
        <p>{{ number }}</p>
        <p>{{ name }}</p>
        <p>{{ type }}</p>
        <div class="element">
        </div>
    </div>
</template>

<style scoped>
.card {
    width: calc(100% / 5 - 10px);
    height: calc(100% / 2 - 10px);
    background-color: aquamarine;
    border-radius: 20px;
}
</style>
