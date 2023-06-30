<script>
export default {
    data() {
        return {

        }
    },
    promps: {
        card: {
            thumb: 'String',
            price: 'String',
            series: 'String'
        }
    }
}
</script>

<template>
    <div class="card">
        <figure>
            <img :src="thumb" :alt="series">
        </figure>

        <h3>{{ series }}</h3>
    </div>
</template>

<style lang="scss" scoped></style>