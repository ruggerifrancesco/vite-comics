<template>
    <section class="my_buy-nav">
        <div class="wrapper">

            <div class="buy-navigation-btn" v-for="product in buySections">
                
            </div>

        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            buySections: [],
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .my_buy-nav {
        height: 200px;
        background-color: $digital-navigation;
    }

    .buy-navigation-btn * {
        outline: 1px solid red;
    }
</style>