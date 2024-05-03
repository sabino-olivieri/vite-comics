<template>
    <a :style="{'font-size' : size}"> {{ text.toUpperCase() }}</a>
</template>

<script>
export default {
    props: {
        text: String,
        size: String,
    }
}
</script>

<style lang="scss" scoped>
@use "../style/_variables.scss" as *;

    a {
        text-align: center;
        display: inline-block;
        padding: 10px 15px;
        border: 2px solid $primary-blue;
        min-width: 100px;
        background-color: $primary-blue;
        color: white;
        font-weight: bold;
        transition: all 0.5s;
        
        &:hover {
            background-color: white;
            color: $primary-blue;
        }
    }
</style>