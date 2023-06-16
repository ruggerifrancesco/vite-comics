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
        cardItem: {
            thumbnail: String,
            price: String,
            series: String,
            type: String,
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