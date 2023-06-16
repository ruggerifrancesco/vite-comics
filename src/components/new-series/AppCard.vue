<template>
    <article>

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
    }
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/variables.scss' as *;


</style>