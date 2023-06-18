<template>
    <div class="socials-container">
        <span class="social-title">Follow Us</span>
        <ul class="m-0">
            <li v-for="social in socialList">
                <a :href="social.link">
                    <img :src="getImagePath(social.srcIcon)" :alt="social.socialName">
                </a>
            </li>
        </ul> 
    </div>

</template>
<script>
export default {
    data() {
        return {
            socialList: [
                {
                    socialName: 'Facebook',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },
                {
                    socialName: 'Twitter',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },
                {
                    socialName: 'Youtube',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },
                {
                    socialName: 'Pinterest',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },
                {
                    socialName: 'Periscope',
                    link: '#',
                    srcIcon: 'footer-facebook.png',
                },                
            ],
        }
    },
    methods: {
        getImagePath: function(img) {
            // Updated the path here and look all the folders parents
            return new URL(`../../assets/social-icons/${img}`, import.meta.url).href;
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

    .socials-container {
        @include flex (row, none, center);
    }

    ul {
        @include flex (row, none, center);
        gap: 1rem;
    }

    .social-title {
    color: $primary-color;
    text-transform: uppercase;
    font-size: 1.5rem;
    font-weight: 600;
    font-family: 'Oswald', sans-serif;
    margin-right: 2.5rem;
}
</style>