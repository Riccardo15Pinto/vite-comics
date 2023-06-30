<script>
import AppJumbo from '../components/AppJumbo.vue';
export default {
    components: { AppJumbo },
    props: {
        comics: 'Array',
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <AppJumbo :comics="comics" />
    <main>

        <nav>
            <div class="column">
                <div>
                    <h3><a href="#">DC COMICS</a></h3>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>
                </div>
                <div>
                    <h3><a href="#">SHOP</a></h3>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>

            </div>
            <div class="column">
                <h3><a href="#">DC</a></h3>
                <ul>
                    <li><a href="#">Terms Of Use</a></li>
                    <li><a href="#">Privacy Policy(New)</a></li>
                    <li><a href="#">Ad Choices</a></li>
                    <li><a href="#">Advertising</a></li>
                    <li><a href="#">Jobs</a></li>
                    <li><a href="#">Subscriptions</a></li>
                    <li><a href="#">Talent Workshops</a></li>
                    <li><a href="#">CPSC Certificates</a></li>
                    <li><a href="#">Ratings</a></li>
                    <li><a href="#">Shop Help</a></li>
                    <li><a href="#">Contact Us</a></li>
                </ul>
            </div>
            <div class="column">
                <h3><a href="#">SITIES</a></h3>
                <ul>
                    <li><a href="#">DC</a></li>
                    <li><a href="#">MAD Magazine</a></li>
                    <li><a href="#">DC Kids</a></li>
                    <li><a href="#">DC Universe</a></li>
                    <li><a href="#">DC Power Visa</a></li>
                </ul>
            </div>
        </nav>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;

    nav {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        width: 1300px;
        margin: 0 auto;
        background-position: right;
        display: flex;

        .column {
            margin-right: 30px;
            padding: 30px 0;

            h3 {
                margin: 10px 0;
            }

            li {
                margin: 5px 0;


            }

            h3 a {
                color: white;
            }

            li a {
                color: #959595;

                &:hover {
                    color: white;
                }
            }
        }
    }
}
</style>