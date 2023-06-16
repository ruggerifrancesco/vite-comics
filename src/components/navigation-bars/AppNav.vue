<template>
    <div class="my_page-logo">
        <img src="../../assets/img/dc-logo.png" alt="DC Main Logo">
    </div>

    <nav>
        <ul class="my_list-nav">
            <li v-for="link in navItems">
                <a :href="link.href">{{ link.item }}</a>
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
                    item: 'Characters',
                    href: '#',
                },
                {
                    id: 2,
                    active: false,
                    item: 'Comics',
                    href: '#',
                },
                {
                    id: 3,
                    active: false,
                    item: 'Movies',
                    href: '#',
                },
                {
                    id: 4,
                    active: false,
                    item: 'Tv',
                    href: '#',
                },
                {
                    id: 5,
                    active: false,
                    item: 'Games',
                    href: '#',
                },
                {
                    id: 6,
                    active: false,
                    item: 'Collectibles',
                    href: '#',
                },
                {
                    id: 7,
                    active: false,
                    item: ' Videos',
                    href: '#',
                },
                {
                    id: 8,
                    active: false,
                    item: 'Fans',
                    href: '#',
                },
                {
                    id: 9,
                    active: false,
                    item: 'News',
                    href: '#',
                },
                {
                    id: 10,
                    active: false,
                    item: 'Shop',
                    href: '#',
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .my_page-logo {
        width: 100px;
    }
    .my_list-nav {
        @include flex (row, none, center);
        gap: 2rem;
    }

    li a {
        font-family: 'Oswald', sans-serif;
        font-size: 1.1rem;
        text-transform: uppercase;
        color: $secondary-color;
    }
</style>