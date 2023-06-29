<script>
export default {
    data() {
        return {
            socials: [
                {
                    pic: 'footer-facebook.png',
                    name: 'facebook',
                    current: false
                },
                {
                    pic: 'footer-periscope.png',
                    name: 'periscope',
                    current: false
                },
                {
                    pic: 'footer-pinterest.png',
                    name: 'pinterest',
                    current: false
                },
                {
                    pic: 'footer-twitter.png',
                    name: 'twitter',
                    current: false
                },
                {
                    pic: 'footer-youtube.png',
                    name: 'youtube',
                    current: false
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

<template></template>

<style lang="scss" scoped></style>