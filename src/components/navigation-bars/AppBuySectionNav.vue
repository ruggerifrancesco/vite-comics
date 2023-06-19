<template>
    <section class="my_buy-nav">
        <div class="wrapper">

            <div class="buy-navigation-btn" v-for="product in buySections">

            </div>

        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            buySections: [
                {
                    iconProduct: 'Digital Comics',
                    link: '#',
                    iconSrc: 'buy-comics-digital-comics.png',
                },
                {
                    iconProduct: 'DC Merchandise',
                    link: '#',
                    iconSrc: 'buy-comics-merchandise.png',
                },
                {
                    iconProduct: 'Subscription',
                    link: '#',
                    iconSrc: 'buy-comics-subscriptions.png',
                },
                {
                    iconProduct: 'Comic Shop Locator',
                    link: '#',
                    iconSrc: 'buy-comics-shop-locator.png',
                },
                {
                    iconProduct: 'DC Power Visa',
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

    .my_buy-nav {
        height: 200px;
        background-color: $digital-navigation;
    }

    .buy-navigation-btn * {
        outline: 1px solid red;
    }
</style>