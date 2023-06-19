<template>
    <ul class="m-0">
        <li>
            <a :href="link">
                <img :src="getImagePath(icon)" :alt="name" class="socialImg-icon">
            </a>
        </li>
    </ul> 
</template>
<script>
export default {
    props: {
        name: String,
        link: String,
        icon: String,
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

    ul {
        @include flex (row, none, center);
    }

    .socialImg-icon:hover {
        filter: brightness(0) invert(1);
    }
</style>