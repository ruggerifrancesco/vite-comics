<template>
    <main>
        <div class="wrapper">
            Content goes Here
        </div>
    </main>
    <AppSpecialNav />
</template>

<script>
import AppSpecialNav from './partials/AppSpecialNav.vue';

export default {
    components: {
        AppSpecialNav
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

    main {
        color: white;
        height: 200px;
        background-color: $main-app-bg;
    }
</style>