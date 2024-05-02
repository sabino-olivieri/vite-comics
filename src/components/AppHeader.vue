<template>

    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>

            <nav>
                <ul>
                    <li v-for="element in navLink" :class="{ 'active': element.active }"><a href="" :class="{ 'active': element.active }">{{
                        element.name.toUpperCase() }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {

    data() {
        return {
            navLink: [
                {
                    name: "characters",
                    active: false
                },
                {
                    name: "comics",
                    active: true
                },
                {
                    name: "movies",
                    active: false
                },
                {
                    name: "tv",
                    active: false
                },
                {
                    name: "games",
                    active: false
                },
                {
                    name: "collectibles",
                    active: false
                },
                {
                    name: "videos",
                    active: false
                },
                {
                    name: "fans",
                    active: false
                },
                {
                    name: "news",
                    active: false
                },
                {
                    name: "shop",
                    active: false
                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;
@use "../style/_variables.scss" as *;

header {
    color: $grey-footer;
    height: $header-height;
    

    .container {
        @include flex(space-between, center);

        nav {
            ul {
                @include flex(center, center);
                gap: 15px;

                li {
                    position: relative;
                    height: $header-height;
                    @include flex(center, center);
                    .active:before {
                        content: "";
                        width: 100%;
                        height: 5px;
                        background-color: $primary-blue;
                        position: absolute;
                        bottom: 0;
                    }

                    &:hover:before {
                        content: "";
                        width: 100%;
                        height: 5px;
                        background-color: $primary-blue;
                        position: absolute;
                        bottom: 0;
                    }
                }


                a {
                    font-weight: bold;
                    font-size: 0.8rem;

                    &:hover {
                        color: $primary-blue;

                    }
                }
            }
        }
    }

    img {
        width: 60px;
    }
}

.active {
    color: $primary-blue;
}
</style>