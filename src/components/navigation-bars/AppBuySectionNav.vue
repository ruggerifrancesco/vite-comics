<template>
    <section class="my_store-nav">
        <div class="wrapper">

            <div v-for="store in storeSections" class="buy-store-section">
                <a :href="store.link">
                    <img :src="getImagePath(store.iconSrc)" :alt="store.iconProduct">
                    <span class=""></span>
                </a>
            </div>

        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            storeSections: [
                {
                    iconStore: 'Digital Comics',
                    link: '#',
                    iconSrc: 'buy-comics-digital-comics.png',
                },
                {
                    iconStore: 'DC Merchandise',
                    link: '#',
                    iconSrc: 'buy-comics-merchandise.png',
                },
                {
                    iconStore: 'Subscription',
                    link: '#',
                    iconSrc: 'buy-comics-subscriptions.png',
                },
                {
                    iconStore: 'Comic Shop Locator',
                    link: '#',
                    iconSrc: 'buy-comics-shop-locator.png',
                },
                {
                    iconStore: 'DC Power Visa',
                    link: '#',
                    iconSrc: 'buy-dc-power-visa.svg',
                },
            ],
        }
    },
    methods: {
        getImagePath: function(img) {
            // Updated the path here and look all the folders parents
            return new URL(`../../assets/products-icons/${img}`, import.meta.url).href;
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .my_store-nav {
        background-color: $digital-navigation;
    }

    .wrapper {
        @include flex (row, center, center);
    }

    .buy-store-section * {
        outline: 1px solid red;

        img {
            width: 5rem;
            aspect-ratio: 1/1;
            object-fit: contain;
        }
    }
</style>