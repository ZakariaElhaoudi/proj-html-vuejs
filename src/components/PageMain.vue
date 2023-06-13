<script>
import SectionCountDown from './SectionCountDown.vue'
import SectionSpeakers from './SectionSpeakers.vue'
import SectionProgram from './SectionProgram.vue'
import SectionMaps from './SectionMaps.vue'
export default {
    name: 'PageMain',
    components: {
        SectionCountDown,
        SectionSpeakers,
        SectionProgram,
        SectionMaps
    },
    data() {
        return {
        }
    }
}
</script>

<template>
    <SectionCountDown />
    <SectionSpeakers />
    <SectionProgram />
    <SectionMaps />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
</style>