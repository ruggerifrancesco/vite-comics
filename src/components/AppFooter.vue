<template>
    <footer>
        <!-- Main Footer -->
        <section class="main-footer">
            <div class="wrapper">

                <div class="links-wrapper">
                    <div class="footer-col">
                        <h4>Dc Comics</h4>
                        <ul>
                            <li v-for="link in dcComicsItemsList">
                                <a :href="link.link">{{ link.item }}</a>
                            </li>
                        </ul>
                        <h4>Shop</h4>
                        <ul>
                            <li v-for="link in shopItemsList">
                                <a :href="link.link">{{ link.item }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>Dc</h4>
                        <ul>
                            <li v-for="link in dcItemsList">
                                <a :href="link.link">{{ link.item }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>Sites</h4>
                        <ul>
                            <li v-for="link in siteItemsList">
                                <a :href="link.link">{{ link.item }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Logo Background -->
                <div class="background-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="background logo">
                </div>
            </div>
        </section>

        <!-- Second Footer -->
        <section class="miscellaneous-footer">
            <div class="wrapper">

            </div>
        </section>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            dcComicsItemsList: [
                {
                    item: 'Characters',
                    link: '#',
                },
                {
                    item: 'Comics',
                    link: '#',
                },
                {
                    item: 'Movies',
                    link: '#',
                },
                {
                    item: 'TV',
                    link: '#',
                },
                {
                    item: 'Games',
                    link: '#',
                },
                {
                    item: 'Videos',
                    link: '#',
                },
                {
                    item: 'News',
                    link: '#',
                },
            ],
            shopItemsList: [
                {
                    item: 'Characters',
                    link: '#',
                },
                {
                    item: 'Comics',
                    link: '#',
                },

            ],
            dcItemsList: [
                {
                    item: 'Term of Use',
                    link: '#',
                },
                {
                    item: 'Privacy Police (New)',
                    link: '#',
                },
                {
                    item: 'Ad Choises',
                    link: '#',
                },
                {
                    item: 'Advertising',
                    link: '#',
                },
                {
                    item: 'Jobs',
                    link: '#',
                },
                {
                    item: 'Subscription',
                    link: '#',
                },
                {
                    item: 'Talent Workshop',
                    link: '#',
                },
                {
                    item: 'CPSC Certificates',
                    link: '#',
                },
                {
                    item: 'Ratings',
                    link: '#',
                },
                {
                    item: 'Shop Help',
                    link: '#',
                },
                {
                    item: 'Contact Us',
                    link: '#',
                },
            ],
            siteItemsList: [
                {
                    item: 'DC',
                    link: '#',
                },
                {
                    item: 'MAD Magazine',
                    link: '#',
                },
                {
                    item: 'DC Kids',
                    link: '#',
                },
                {
                    item: 'DC Universe',
                    link: '#',
                },
                {
                    item: 'DC Power Visa',
                    link: '#',
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/_mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

    footer {
        height: 550px;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        position: relative;
        color: white;
        overflow: hidden;
    }
    .background-logo {
        position: absolute;
        top: -4rem;
        right: 0;

    }
    .wrapper {
        @include flex (row, space-between, flex-start);
        position: relative;
    }
    .links-wrapper {
        @include flex (row, none, flex-start);
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