<script>
import axios from 'axios'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
export default {
    name: 'pokemonlist',
    data: () => ({ characters: [] }),
    created() {
        axios.get(endpoint).then(res => {
            console.log(res)
        })
    }
}
</script>

<template></template>

<style scoped></style>
