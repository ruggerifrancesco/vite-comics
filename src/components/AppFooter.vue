<template>
    <footer>
        <!-- Main Footer -->
        <section class="main-footer">
            <div class="wrapper">

                <div class="links-wrapper">
                    <div class="footer-col">

                        <h4>Dc Comics</h4>
                        <ul class="list-container">
                            <FooterLinksDcComics v-for="referral in dcComicsItemsList"
                                :item="referral.item"
                                :link="referral.link"
                                />
                        </ul>

                        <h4>Shop</h4>
                        <ul>
                            <FooterLinksShopVue v-for="referral in shopItemsList"
                                :item="referral.item"
                                :link="referral.link"
                                />
                        </ul>

                    </div>

                    <div class="footer-col">

                        <h4>Dc</h4>
                        <ul>
                            <FooterLinksDc v-for="referral in dcItemsList"
                                :item="referral.item"
                                :link="referral.link"
                                />
                        </ul>

                    </div>

                    <div class="footer-col">

                        <h4>Sites</h4>
                        <ul>
                            <FooterLinksSites v-for="referral in siteItemsList"
                                :item="referral.item"
                                :link="referral.link"
                                />
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

                    <div class="socials-container">
                        <span class="social-title">Follow Us</span>
                    <AppSocialsListVue v-for="social in socialList"
                        :name="social.socialName"
                        :link="social.link"
                        :icon="social.srcIcon"/>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>

<script>
import FooterLinksDcComics from './footer-components/FooterLinksDcComics.vue';
import FooterLinksShopVue from './footer-components/FooterLinksShop.vue';
import FooterLinksDc from './footer-components/FooterLinksDc.vue';
import FooterLinksSites from './footer-components/FooterLinksSites.vue';
import AppSocialsListVue from './footer-components/AppSocialsList.vue';

export default {
    components: {
        FooterLinksDcComics,
        FooterLinksShopVue,
        FooterLinksDc,
        FooterLinksSites,
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
            socialList: [
                {
                    socialName: 'Facebook',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },
                {
                    socialName: 'Twitter',
                    link: '#',
                    srcIcon: 'footer-twitter.png',
                },
                {
                    socialName: 'Youtube',
                    link: '#',
                    srcIcon: 'footer-youtube.png',
                },
                {
                    socialName: 'Pinterest',
                    link: '#',
                    srcIcon: 'footer-pinterest.png',
                },
                {
                    socialName: 'Periscope',
                    link: '#',
                    srcIcon: 'footer-periscope.png',
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
    .list-container {
        margin-bottom: 1.4rem;
    }
    h4 {
        margin-bottom: 1rem;
        text-transform: uppercase;
        font-family: 'Oswald', sans-serif;
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

    .socials-container {
        @include flex (row, none, center);
        gap: 1rem;
    }
    .social-title {
        color: $primary-color;
        text-transform: uppercase;
        font-size: 1.5rem;
        font-weight: 600;
        font-family: 'Oswald', sans-serif;
        margin-right: 1.5rem;
    }

</style>