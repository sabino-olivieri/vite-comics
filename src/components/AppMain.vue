<template>
    <main>
        <div class="container">
            <h1>--> Content goes here <--</h1>
        </div>
    </main>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;

main {
    height: 100px;
    background-color: black;
    @include flex(start, center);

    h1 {
        color: white;
    }
}
</style>