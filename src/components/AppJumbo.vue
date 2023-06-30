<script>
import ComicCard from './ComicCard.vue'
export default {
    data() {
        return {
            images: [
                {
                    pic: 'buy-comics-digital-comics.png',
                    name: 'DIGITAL COMICS',
                    current: false
                },
                {
                    pic: 'buy-comics-merchandise.png',
                    name: 'DC MERCHANDISE',
                    current: false
                },
                {
                    pic: 'buy-comics-shop-locator.png',
                    name: 'SUBSCRIPTION',
                    current: false
                },
                {
                    pic: 'buy-comics-subscriptions.png',
                    name: 'COMIC SHOP LOCATOR',
                    current: false
                },
                {
                    pic: 'buy-dc-power-visa.svg',
                    name: 'DC POWER VISA',
                    current: false
                }
            ]
        }
    },
    promps: {
        comics: 'Array',
    },
    methods: {
        getImagePath(target) {
            const url = new URL(`../assets/img/${target}`, import.meta.url)
            return url.href
        }
    },
    components: { ComicCard }
}
</script>

<template>
    <section class="jumbo-section">
        <div class="top-jumbo">
            <h2>Current Series</h2>
        </div>
        <div class="bottom-jumbo">
            <div class="container-card">
                <ComicCard v-for="comic in comics" :card=comics :thumb="comic" :price="comic" :series="comic"
                    :key="comic.series" />
            </div>
        </div>
    </section>
    <section class="info-merch">

        <div>
            <ul>
                <li v-for="image in images" :key="image.name">
                    <figure>
                        <img :src="getImagePath(image.pic)" alt="">
                    </figure>
                    <span>{{ image.name }}</span>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.jumbo-section {
    .top-jumbo {
        background-image: url('../assets/img/jumbotron.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        height: 400px;

        h2 {
            background-color: #0282F9;
            padding: 10px 20px;
            display: inline-block;
            text-transform: uppercase;
            color: white;
        }
    }

    .bottom-jumbo {
        background-color: #1C1C1C;
        padding: 40px 0;
        color: white;

        .container-card {
            margin: 0 auto;
            width: 1300px;
            display: flex;
            flex-wrap: wrap;

            .card {
                flex-basis: calc(100% / 6);
            }
        }
    }
}

.info-merch {
    background-color: #0282F9;

    div {
        padding: 40px 0;
        width: 1300px;
        margin: 0 auto;
        color: white;

        ul {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;

            li {
                display: flex;
                justify-content: space-between;
                align-items: center;

                figure {
                    width: 50px;
                }

                span {
                    margin-left: 10px;
                }
            }
        }
    }
}
</style>