<template>
    <section class="blu-banner">
        <div class="container">
            <ul>
                <li v-for="element in bannerList">
                    <a href="">
                        <img :src="getImagePath(element.image)" alt="">
                        <span>{{ element.name.toUpperCase() }}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            bannerList: [
                {
                    image: "buy-comics-digital-comics.png",
                    name: "digital comics"
                },
                {
                    image: "buy-comics-merchandise.png",
                    name: "dc merchandise"
                },
                {
                    image: "buy-comics-subscriptions.png",
                    name: "subscription"
                },
                {
                    image: "buy-comics-shop-locator.png",
                    name: "comic shop locator"
                },
                {
                    image: "buy-dc-power-visa.svg",
                    name: "dc power visa"
                },
                
            ]
        }

    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;

.container {
    padding: 40px 10px;
    @include flex(center, center);

    ul {
        @include flex(space-between, center);
        color: white;
        width: 100%;


        li a{
            @include flex(space-between, center);
            gap: 10px;
            font-size: 0.8rem;
            text-wrap: nowrap;
        }

        img {
            max-height: 40px;
            max-width: 40px;
        }
    }
}

.blu-banner {
    background-color: blue;
    @include flex(center, center);
}
</style>