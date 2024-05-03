<template>
    <main>
        <div class="jumbotron">

        </div>


        <div class="container">
            <AppButton class="btn" text="current series" size="1rem" />
        </div>
    </main>
</template>

<script>
import AppButton from './AppButton.vue';

export default {
    components: {
        AppButton
    },

}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;

main {

    background-color: black;

    .jumbotron {
        height: 350px;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;
        background-position: top;
        
    }

    .container {
        padding: 20px 0;
        position: relative;
        .btn {
            position: absolute;
            top: -50%;
            left: 0;
        }
    }


    h1 {
        color: white;
    }
}
</style>