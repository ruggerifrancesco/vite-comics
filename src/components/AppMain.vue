<template>
    <main>
        <div class="wrapper">
            <h1>{{ contentHere }}</h1>
        </div>
    </main>
    <AppSpecialNav />
</template>

<script>
import AppSpecialNav from './navigation-bars/AppSpecialNav.vue';

export default {
    name: AppMain,
    components: {
        AppSpecialNav
    },
    data() {
        return {
           contentHere: '--> Content Goes Here <--', 
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/_mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

    main {
        color: white;
        height: 160px;
        background-color: $main-app-bg;
        @include flex (row, none, center);
    }

    h1 {
        margin-bottom: 0;
    }
</style>