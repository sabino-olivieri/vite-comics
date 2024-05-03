<template>
    <footer class="main-footer">
        <div class="container">
            <div class="col">
                <div v-for="element in listFooter">
                <h2>{{ element.name.toUpperCase() }}</h2>

                <ul>
                    <li v-for="item in element.link"><a href="">{{ item }}</a></li>
                </ul>
            </div>
            </div>
            

        </div>

    </footer>
</template>

<script>
export default {
    data() {
        return {
            listFooter: [
                {
                    name: "dc comics",
                    link: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    name: "shop",
                    link: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    name: "dc",
                    link: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratinngs", "Shop Help", "Contact Us"]
                },
                {
                    name: "sites",
                    link: ["DC", "MAD Magazine", "DC Kids", "DC Univers", "DC Power Visa"]
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use "../style/_mixin.scss" as *;

.main-footer {
    
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;

    .container {
        
        
        padding: 20px 0;
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: right;
        color: white;
        height: 100%;

        .col {
            @include flex(center, start);
            flex-direction: column;
            flex-wrap: wrap;
            max-height: 350px;
            width: 50%;
        }

        h2 {
            margin: 10px 0;
        }

        li {
            margin: 5px 0;

            a {
                font-size: 0.8rem;
                color: #959595;
                &:hover {
                    text-decoration: underline;
                }
            }
        }
    }

}
</style>