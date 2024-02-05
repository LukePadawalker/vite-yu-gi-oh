<script>
import store from '../store.js'
import AppComponents from './AppComponents.vue'
export default {
    data() {
        return {
            store,
        }
    }

}
</script>

<template>
    <div class="background">
        <div class="container">
            <AppComponents />

        </div>
    </div>
</template>

<style lang="scss" scoped>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

.background {
    width: 100%;
    height: 100vh;
    background-color: red;
    display: flex;
    justify-content: center;
    align-items: center;

    .container {
        width: 70%;
        height: 60%;
        background-color: rgb(219, 216, 216);
        overflow: scroll;
    }
}
</style>
