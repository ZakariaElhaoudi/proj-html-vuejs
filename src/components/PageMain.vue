<script>
import SectionCountDown from './SectionCountDown.vue'
import SectionSpeakers from './SectionSpeakers.vue'
import SectionProgram from './SectionProgram.vue'
import SectionMaps from './SectionMaps.vue'
import SectionLocation from './SectionLocation.vue'
import SectionRecentNews from './SectionRecentNews.vue'
export default {
    name: 'PageMain',
    components: {
        SectionCountDown,
        SectionSpeakers,
        SectionProgram,
        SectionMaps,
        SectionLocation,
        SectionRecentNews
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
    <SectionLocation />
    <SectionRecentNews />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
</style>