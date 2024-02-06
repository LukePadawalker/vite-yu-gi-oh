<script>
import { store } from '/src/store.js';
export default {
    img: store.imageUrl,
    number: store.number,
    name: store.name,
    type: store.type1,


}
</script>

<template>
    <div class="card">
        <img :src="img" alt="">
        <div class="number">
            <p>{{ number }}</p>
        </div>
        <div class="name">
            <p>{{ name }}</p>
        </div>
        <div class="element">
            <p>{{ type }}</p>
        </div>
    </div>
</template>

<style scoped>
.card {
    width: calc(100% / 5);
    height: calc(100% / 2);
    background-color: aquamarine;
}
</style>
