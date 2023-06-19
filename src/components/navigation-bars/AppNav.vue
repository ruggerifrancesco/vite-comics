<template>
    <nav>
        <ul class="my_list-nav">
            <li v-for="(link, index) in navItems" :key="index" @click="setActive(index)" :class="{ active: link.active }">
                <a :href="link.href" :class="{ active: link.active }">{{ link.item }}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'AppNav',
    data() {
        return {
            navItems: [
                {
                    active: false,
                    item: 'Characters',
                    href: '#',
                },
                {
                    active: true,
                    item: 'Comics',
                    href: '#',
                },
                {
                    active: false,
                    item: 'Movies',
                    href: '#',
                },
                {
                    active: false,
                    item: 'Tv',
                    href: '#',
                },
                {
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
                    active: false,
                    item: ' Videos',
                    href: '#',
                },
                {
                    active: false,
                    item: 'Fans',
                    href: '#',
                },
                {
                    active: false,
                    item: 'News',
                    href: '#',
                },
                {
                    active: false,
                    item: 'Shop',
                    href: '#',
                },
            ]
        }
    },
    methods: {
        setActive(index) {
          this.navItems.forEach((item, i) => {
            item.active = i === index;
          });
        },
    } 
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .my_list-nav {
        @include flex (row, none, center);
        gap: 2rem;
    }

    li {
        position: relative;

        a {
            font-family: 'Oswald', sans-serif;
            font-size: 1.1rem;
            text-transform: uppercase;
            color: $secondary-color;
            
            &.active {
                color: $primary-color;
            }
        }
      
        &.active::after {
            content: '';
            height: 5px;
            background-color: $primary-color;
            position: absolute;
            width: 100%;
            left: 0;
            bottom: -3.8rem;
        }
    }
</style>