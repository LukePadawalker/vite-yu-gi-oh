<script>
import AppComponents from './AppComponents.vue'
export default {
    components: { AppComponents }

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

        <div class="container">
            <AppComponents />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.background {
    width: 100%;
    height: 100vh;
    background-color: rgb(189, 0, 0);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .container {
        width: 70%;
        height: 60%;
        background-color: rgb(219, 216, 216);
        overflow: scroll;
        border-radius: 20px;
    }

    .circle-container {
        width: 70%;
        height: 110px;
        padding: 10px;
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        justify-content: flex-start;
        gap: 10px;

        .blue-circle {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 4px solid lightgrey;
            background-color: blue;
            background-image: linear-gradient();
            align-self: flex-end;
        }

        .red-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 4px solid lightgrey;
            background-color: rgb(255, 0, 0);
            background-image: linear-gradient();
        }

        .yellow-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 4px solid lightgrey;
            background-color: rgb(219, 252, 0);
            background-image: linear-gradient();
        }

        .green-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 4px solid lightgrey;
            background-color: rgb(0, 255, 42);
            background-image: linear-gradient();
        }
    }


}
</style>
