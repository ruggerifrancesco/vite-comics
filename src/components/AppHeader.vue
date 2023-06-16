<template>
    <header class="my_header">
        <div class="wrapper">
            <div class="my_page-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
            </div>
            <AppNav />
        </div>
    </header>
</template>

<script>
import AppNav from './partials/AppNav.vue';

export default {
    name: AppHeader,
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

    .wrapper {
        @include flex (row, space-between, center);
        padding: 1.5rem 0;
    }
</style>