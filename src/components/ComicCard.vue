<script>
export default {
    data() {
        return {

        }
    },
    props: {
        comic: 'Object'
    }
}
</script>

<template>
    <div class="card">
        <figure>
            <img :src="comic.thumb" :alt="comic.series">
        </figure>

        <h3>{{ comic.series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
.card {
    padding: 20px;

    figure {
        background-color: black;
    }


    img {
        height: 300px;

        &:hover {
            opacity: 0.3;
        }

    }
}
</style>