<script>
import L from "leaflet";
import "leaflet-control-geocoder";
export default {
    name: 'SectionMaps',

    data() {
        return {
            address: "1000 5th Ave, New York, NY 10028, Stati Uniti"
        }
    },
    methods: {
        initializeMap() {
            const map = L.map("map").setView([0, 0], 13);

            L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
                attribution: "© OpenStreetMap contributors",
                maxZoom: 19
            }).addTo(map);

            const geocoder = L.Control.Geocoder.nominatim();

            geocoder.geocode(this.address, (results) => {
                if (results.length > 0) {
                    const location = results[0].center;
                    map.setView(location, 13);
                    L.marker(location).addTo(map);
                }
            });
        }
    },
    mounted() {
        this.initializeMap();
    },
}
</script>

<template>
    <section>
        <div id="map"></div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

#map {
    height: 400px;
    width: 100%;
}
</style>