<template>
    <article class="card-item">
        <img src="" alt="">
    </article>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    props: {
        singleCard: {
            thumbnail: String,
            price: String,
            series: String,
            type: String,
        }
    },
    methods: {
        getImagePath: function(img) {
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/variables.scss' as *;

    .card-item {
        background-color: $card-bg;
        width: $card-w-h;
        height: $card-w-h;
        outline: 1px solid red;
    }
</style>