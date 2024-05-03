<template>
    <div class="card">
        <div class="cover">
            <img :src="getImagePath(thumb)" :alt="series">
            <div class="price">
                {{ price }}
            </div>
        </div>
        <p>
            {{ series.toUpperCase() }}
        </p>
    </div>
</template>

<script>
export default {
    props: {
        thumb: String,
        series: String,
        price: String,
    },

    methods: {
        getImagePath(img) {
            return new URL(`${img}`, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
    .card {

        transition: all 0.5s;

        &:hover {
            transform: scale(110%);
            background-color: white;
            color: black;
            border-radius: 10px;

            img {
                border-radius: 10px 10px 0 0;
            }

            p {
                padding-left: 10px;
            }

            .price {
                border-radius: 0 10px 0 10px;
            }

        }

        .cover {

            position: relative;
            
            img {
                width: 100%;
                aspect-ratio: 1 /1 ;
                object-fit: cover;
                transition: all 0.5s;
                

            }
        }

        p {
            text-align: start;
            padding: 10px 0;
            font-size: 0.8rem;
            transition: padding-left 0.5s;
        }

        .price {
            padding: 5px;
            background-color: rgb(1, 97, 1);
            color: white;
            border-radius: 0 0 0 10px;
            position: absolute;
            right: 0;
            top: 0;
            z-index: 999;
            transition: all 0.5s;
        }
    }
</style>