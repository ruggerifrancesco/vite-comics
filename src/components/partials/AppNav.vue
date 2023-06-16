<template>
    <nav>
        <ul class="my_list-nav">
            <li v-for="link in navItems">
                <a href="#">{{ link.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            navItems: [
                {
                    id: 1,
                    active: false,
                    name: 'Characters',
                },
                {
                    id: 2,
                    active: false,
                    name: 'Comics',
                },
                {
                    id: 3,
                    active: false,
                    name: 'Movies',
                },
                {
                    id: 4,
                    active: false,
                    name: 'Tv',
                },
                {
                    id: 5,
                    active: false,
                    name: 'Games',
                },
                {
                    id: 6,
                    active: false,
                    name: 'Collectibles',
                },
                {
                    id: 7,
                    active: false,
                    name: ' Videos',
                },
                {
                    id: 8,
                    active: false,
                    name: 'Fans',
                },
                {
                    id: 9,
                    active: false,
                    name: 'News',
                },
                {
                    id: 10,
                    active: false,
                    name: 'Shop',
                },
            ]
        }
    },
}
</script>

<style lang="scss">
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .my_list-nav {
        @include flex (row, none, center);
        gap: 1rem;
    }
</style>