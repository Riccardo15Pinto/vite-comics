<script>
export default {
    data() {
        return {
            items: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div>

            <figure>
                <img src="../assets/img/dc-logo.png" alt="">
            </figure>
            <ul>
                <li v-for="item in items" :key="item.text"><a :href="item.url">{{ item.text }}</a></li>
            </ul>
        </div>

    </header>
</template>

<style lang="scss" scoped>
header {
    height: 150px;

    div {
        display: flex;
        justify-content: space-between;
        width: 1300px;
        margin: 0 auto;
        padding: 20px 0;

        ul {
            display: flex;
            align-items: center;

            li {
                margin-left: 20px;

                a {
                    font-weight: 600;
                    text-transform: uppercase;
                    color: black;
                    padding: 60px 0;

                    &:hover,
                    &:focus {
                        color: #0C7CEC;
                        border-bottom: 5px solid currentColor;
                    }
                }
            }
        }
    }
}
</style>