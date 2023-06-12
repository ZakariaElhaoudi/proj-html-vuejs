<script>
import SectionCountDown from './SectionCountDown.vue'
export default {
    name: 'PageMain',
    components: {
        SectionCountDown
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <SectionCountDown />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
</style>