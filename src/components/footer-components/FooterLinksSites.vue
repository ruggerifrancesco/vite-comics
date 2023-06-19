<template>
    <li>
        <a :href="link">{{ item }}</a>
    </li>
</template>
<script>
export default {
props: {
    item: String,
    link: String,
}
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/_mixins.scss' as *;
@use '../../styles/partials/_variables.scss' as *;

li a {
    color: $footer-links;
    font-size: 0.92rem;
}
</style>