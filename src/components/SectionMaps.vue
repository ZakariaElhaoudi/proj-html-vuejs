<script>
import { computed } from "vue";
import { useGeolocation } from "../useGeolocation";
export default {
    name: 'SectionMaps',
    data() {
        const { coords } = useGeolocation()
        const currPos = computed(() => ({
            lat: coords.value.latitude,
            lng: coords.value.longitude
        }))
        return {
            currPos
        }
    },
}
</script>

<template>
    <section class="container-fluid bg-light">
        <div class="m-auto">
            <h4>Your Position</h4>
            Latitude: {{ currPos.lat.toFixed(2) }},
            Longitude: {{ currPos.lng.toFixed(2) }}
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

.m-auto {
    height: 400px;
    width: 100%;
}
</style>