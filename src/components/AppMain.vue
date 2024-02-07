<script>
import PokemonContainer from './PokemonContainer.vue'
import TypeSelect from './TypeSelect.vue'
import { store } from '/src/data/store.js'

export default {
    components: { PokemonContainer, TypeSelect },
    data: () => ({ store }),
    emits: ["read-value"]

}
</script>

<template>
    <div class="background">
        <div class="circle-container">
            <div class="blue-circle"></div>
            <div class="red-circle"></div>
            <div class="yellow-circle"></div>
            <div class="green-circle"></div>
        </div>

        <TypeSelect class="type-select" @option-change="$emit('read-value', currentOption)" :options="store.types"
            default-label="tutti i tipi" />
        <div class="container">
            <PokemonContainer />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.background {
    width: 100%;
    height: 100vh;
    background-color: rgb(141, 0, 0);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .container {
        width: 70%;
        height: 60%;
        background-color: rgb(192, 192, 192);
        overflow: scroll;
        border-radius: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .circle-container {
        width: 70%;
        height: 110px;
        padding: 15px;
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        justify-content: flex-start;
        gap: 10px;

        .blue-circle {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 5px solid lightgrey;
            background-image: linear-gradient(to top left, blue, white, );
            align-self: flexend;
        }

        .red-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 5px solid lightgrey;
            background-image: linear-gradient(to top left, rgb(255, 0, 0), white, );
        }

        .yellow-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 5px solid lightgrey;
            background-image: linear-gradient(to top left, rgb(246, 255, 0), white, );
        }

        .green-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 5px solid lightgrey;
            background-image: linear-gradient(to top left, rgb(12, 122, 17), white, );
        }

        .type-select {
            justify-self: flex-end;
        }
    }


}
</style>
