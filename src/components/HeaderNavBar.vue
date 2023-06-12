<script>
export default {
    name: 'HeaderNavBar',
    props: {
        linkNav: Object
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <li class="px-1 ">
        <a :href="linkNav.link">{{ linkNav.text }}</a>
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

li a {
    font-weight: 600;
    transition: background 0.3s;

    &.active,
    &:hover {
        color: red;
        padding-bottom: 1em;
        border-bottom: solid 2px red;
    }
}
</style>