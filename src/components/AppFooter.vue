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
                                <a :href="link.href">{{ link.item }}</a>
                            </li>
                        </ul>
                        <h4>Shop</h4>
                        <ul>
                            <li v-for="link in shopItemsList">
                                <a :href="link.href">{{ link.item }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>Dc</h4>
                        <ul>
                            <li v-for="link in dcItemsList">
                                <a :href="link.href">{{ link.item }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>Sites</h4>
                        <ul>
                            <li v-for="link in siteItemsList">
                                <a :href="link.href">{{ link.item }}</a>
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

                <div class="miscellaneous-wrapper">
                    <div class="signUp-btn-container">
                        <button type="button" class="btn btn-outline-primary" id="signUp-btn">
                            Sign Up Now!
                        </button>
                    </div>

                    <AppSocialsListVue />
                </div>
            </div>
        </section>
    </footer>
</template>

<script>
import AppSocialsListVue from './related-socials/AppSocialsList.vue';

export default {
    components: {
        AppSocialsListVue,
    },
    data() {
        return {
            dcComicsItemsList: [
                {
                    item: 'Characters',
                    href: '#',
                },
                {
                    item: 'Comics',
                    href: '#',
                },
                {
                    item: 'Movies',
                    href: '#',
                },
                {
                    item: 'TV',
                    href: '#',
                },
                {
                    item: 'Games',
                    href: '#',
                },
                {
                    item: 'Videos',
                    href: '#',
                },
                {
                    item: 'News',
                    href: '#',
                },
            ],
            shopItemsList: [
                {
                    item: 'Shop DC',
                    href: '#',
                },
                {
                    item: 'Shop DC Collectibles',
                    href: '#',
                },

            ],
            dcItemsList: [
                {
                    item: 'Term of Use',
                    href: '#',
                },
                {
                    item: 'Privacy Police (New)',
                    href: '#',
                },
                {
                    item: 'Ad Choises',
                    href: '#',
                },
                {
                    item: 'Advertising',
                    href: '#',
                },
                {
                    item: 'Jobs',
                    href: '#',
                },
                {
                    item: 'Subscription',
                    href: '#',
                },
                {
                    item: 'Talent Workshop',
                    href: '#',
                },
                {
                    item: 'CPSC Certificates',
                    href: '#',
                },
                {
                    item: 'Ratings',
                    href: '#',
                },
                {
                    item: 'Shop Help',
                    href: '#',
                },
                {
                    item: 'Contact Us',
                    href: '#',
                },
            ],
            siteItemsList: [
                {
                    item: 'DC',
                    href: '#',
                },
                {
                    item: 'MAD Magazine',
                    href: '#',
                },
                {
                    item: 'DC Kids',
                    href: '#',
                },
                {
                    item: 'DC Universe',
                    href: '#',
                },
                {
                    item: 'DC Power Visa',
                    href: '#',
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
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        position: relative;
        color: white;
    }
    ul {
        margin-bottom: 1.4rem;
    }
    h4 {
        margin-bottom: 1rem;
        text-transform: uppercase;
        font-family: 'Oswald', sans-serif;
    }
    li a {
        color: $footer-links;
        font-size: 0.92rem;
    }
    .main-footer {
        padding: 2.5rem 0;
        overflow: hidden;
    }
    .background-logo {
        position: absolute;
        top: -6rem;
        right: 0;
    }
    .wrapper {
        position: relative;
    }
    .links-wrapper {
        @include flex (row, none, flex-start);
        gap: 3rem;
    }

    .miscellaneous-footer {
        background-color: $second-footer-bg;
        padding: 2rem 0;
    }

    .miscellaneous-wrapper {
       @include flex (row, space-between, center); 
    }

    #signUp-btn {
        color: white;
        border-radius: 0;
        border-width: 3px;
        text-transform: uppercase;
        font-size: 1.2rem;
    }

</style>