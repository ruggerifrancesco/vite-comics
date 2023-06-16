<template>
    <article class="card-item">

        <div class="card-img">
            <img :src="thumbnail" alt="">
        </div>

        <div class="card-infos">
            <h5>Test</h5>
            <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
            </p>
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
        width: calc((100% / 6) - 1.5rem);
        aspect-ratio: 1/1;
        margin-bottom: 1.5rem;
        margin-left: 1.5rem;
        color: black;
    }
</style>