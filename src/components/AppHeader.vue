<template>
    <header class="my_header">
        <div class="my_page-logo">
            <img src="../assets/img/dc-logo.png" alt="DC Main Logo">
        </div>
        <AppNav />
    </header>
</template>

<script>
import AppNav from './partials/AppNav.vue';

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

<style lang="scss">
    .my_page-logo {
        width: 100px;
    }
    .my_header {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>