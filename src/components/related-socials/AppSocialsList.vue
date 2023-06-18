<template>
    <div class="socials-container">
        <span class="social-title">Follow Us</span>
        <ul class="m-0">
            <li v-for="social in socialList">
                <a href="#">
                    <img src="../../assets/img/footer-facebook.png" alt="Facebook link">
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
                    social: 'Facebook',
                    link: '#',
                    srcIcon: '../../assets/img/footer-facebook.png',
                },
                {
                    social: 'Facebook',
                    link: '#',
                    srcIcon: '../../assets/img/footer-facebook.png',
                },
                {
                    social: 'Facebook',
                    link: '#',
                    srcIcon: '../../assets/img/footer-facebook.png',
                },
                {
                    social: 'Facebook',
                    link: '#',
                    srcIcon: '../../assets/img/footer-facebook.png',
                },
                {
                    social: 'Facebook',
                    link: '#',
                    srcIcon: '../../assets/img/footer-facebook.png',
                },                
            ],
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