<template>
    <article class="card-item">

        <div class="card-img">
            <img :src="thumbnail" alt="">
        </div>

        <div class="card-infos">
            <h5>{{ series }}</h5>
        </div>
        
    </article>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    props: {
        thumbnail: String,
        price: String,
        series: String,
        type: String,
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/variables.scss' as *;

    .card-item {
        width: calc((100% / 6) - 2rem);
        margin-bottom: 1.5rem;
        margin-left: 2rem;
    }

    .card-img {
        aspect-ratio: 1/1;
        
        img {
            object-fit: cover;
            object-position: top;
        }
    }

    h5 {
        font-family: 'Lato', sans-serif;
        text-transform: uppercase;
        color: white;
        font-size: 1rem;
        margin-top: 2rem;
    }
</style>