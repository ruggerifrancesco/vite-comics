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
                    item: 'Shop DC',
                    link: '#',
                },
                {
                    item: 'Shop DC Collectibles',
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