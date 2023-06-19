<template>
    <section class="my_store-nav">
        <div class="wrapper">

            <div v-for="store in storeSections" class="buy-store-section">
                <a :href="store.link">
                    <div class="store-context">
                        <img :src="getImagePath(store.iconSrc)" :alt="store.nameStore">
                        <span class="store-label">
                            {{ store.nameStore }}
                        </span>
                    </div>
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
                    nameStore: 'Digital Comics',
                    link: '#',
                    iconSrc: 'buy-comics-digital-comics.png',
                },
                {
                    nameStore: 'DC Merchandise',
                    link: '#',
                    iconSrc: 'buy-comics-merchandise.png',
                },
                {
                    nameStore: 'Subscription',
                    link: '#',
                    iconSrc: 'buy-comics-subscriptions.png',
                },
                {
                    nameStore: 'Comic Shop Locator',
                    link: '#',
                    iconSrc: 'buy-comics-shop-locator.png',
                },
                {
                    nameStore: 'DC Power Visa',
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
        @include flex (row, space-around, center);
    }

    .buy-store-section * {
        outline: 1px solid red;

        img {
            width: 5rem;
            aspect-ratio: 1/1;
            object-fit: contain;
        }
    }

    .store-context {
        @include flex (row, none, center);
    }
</style>