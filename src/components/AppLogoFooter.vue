<template>
    <footer class="social-footer">
        <div class="container">
            <a class="btn" href="">sign-up now</a>

            <div class="col">
                <span>follow us</span>

                <ul>
                    <li v-for="item in listLogo"><a href=""><img :src="getImagePath(item)" :alt="`Logo ${item}`"></a></li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {

    data() {
        return {
            listLogo: ["facebook.png", "twitter.png", "youtube.png", "pinterest.png", "periscope.png"]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/footer-${img}`, import.meta.url).href;
        }
    }

}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;
@use "../style/_variables.scss" as *;

.social-footer {
    background-color: #222222;
}

.container {
    padding: 30px 0;
    @include flex(space-between, center);

    .btn {
        text-transform: uppercase;
        color: white;
        padding: 10px;
        border: 2px solid $primary-blue;
        transition: background-color 0.5s;

        &:hover {
            background-color: $primary-blue;
        }

    }

    .col {
        @include flex(center, center);
        gap: 15px;
        span {
            text-transform: uppercase;
            color: $primary-blue;
            font-weight: bold;
        }

        ul {
            @include flex(center, center);
            gap: 15px;

            img {
                border-radius: 50%;
                transition: background-color 0.5s;
            }

            img:hover {
                background-color: $primary-blue;
            }
        }
    }
}
</style>