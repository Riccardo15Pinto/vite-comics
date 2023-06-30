<script>
export default {
    data() {
        return {
            socials: [
                {
                    picture: 'footer-facebook.png',
                    name_social: 'facebook',
                    isValid: false
                },
                {
                    picture: 'footer-periscope.png',
                    name_social: 'periscope',
                    isValid: false
                },
                {
                    picture: 'footer-pinterest.png',
                    name_social: 'pinterest',
                    isValid: false
                },
                {
                    picture: 'footer-twitter.png',
                    name_social: 'twitter',
                    isValid: false
                },
                {
                    picture: 'footer-youtube.png',
                    name_social: 'youtube',
                    isValid: false
                }
            ]
        }
    },
    methods: {
        getImagePath(target) {
            const url = new URL(`../assets/img/${target}`, import.meta.url)
            return url.href
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <a href="#" class="button">SING-UP NOW!</a>
            <div class="social">
                <h2>FOLLOW US</h2>
                <ul>
                    <li v-for="social in socials" :key="social.name_social">
                        <a href="#">
                            <figure>
                                <img :src="getImagePath(social.picture)" :alt="social.name_social">
                            </figure>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-color: #303030;
    display: flex;
    align-items: center;

    .container {
        width: 1300px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 30px 0;

        .button {
            padding: 20px 30px;
            border: 2px solid #1182F9;
            color: white;
            font-weight: 600;
        }

        .social {
            display: flex;
            align-items: center;

            h2 {
                color: #1182F9;
            }

            ul {
                display: flex;
                align-items: center;
                justify-content: space-between;

                li {
                    margin-left: 20px;
                }
            }
        }
    }
}
</style>