<script>
import SectionFooterTop from './SectionFooterTop.vue'
import SectionFooterBottom from './SectionFooterBottom.vue'
export default {
    name: 'PageFooter',
    components: {
        SectionFooterTop,
        SectionFooterBottom
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <SectionFooterTop />
    <SectionFooterBottom />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;
</style>