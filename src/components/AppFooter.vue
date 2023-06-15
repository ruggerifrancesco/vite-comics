<template>
    <footer>
        <!-- Main Footer -->
        <section class="main-footer">

        </section>

        <!-- Second Footer -->
        <section class="miscellaneous-footer">

        </section>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/_mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

    footer {
        height: 600px;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        position: relative;
    }

    .miscellaneous-footer {
        background-color: $second-footer-bg;
        height: 150px;
        position: absolute;
        bottom: 0;
        right: 0;
        left: 0;
    }
</style>