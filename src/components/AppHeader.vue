<template>
    <header class="my_header">

        <div class="wrapper">
            <div class="my_page-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
            </div>
            <AppNav />
        </div>

        <section class="my_hero-section"></section>
    </header>
</template>

<script>
import AppNav from './navigation-bars/AppNav.vue';

export default {
    components: {
        AppNav
    },
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/_mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    .my_page-logo {
        width: 100px;
    }
    .my_header {
        background-color: $header;
    }

    .my_hero-section {
        background-image: url(../assets/img/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        height: 600px;
    }

    .wrapper {
        @include flex (row, space-between, center);
        padding: 1.5rem 0;
    }
</style>