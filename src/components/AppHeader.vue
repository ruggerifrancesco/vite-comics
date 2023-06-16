<template>
    <header class="my_header">
        <div class="wrapper">
            <AppNav />
        </div>
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

    .wrapper {
        @include flex (row, space-between, center);
        padding: 1.5rem 0;
    }
</style>