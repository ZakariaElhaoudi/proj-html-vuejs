<script>
import SectionWhoWeAre from './SectionWhoWeAre.vue'
import HeaderNavBar from './HeaderNavBar.vue'
export default {
    name: 'PageHeader',
    components: {
        HeaderNavBar,
        SectionWhoWeAre,
    },
    data() {
        return {
            links: [
                {
                    link: '#',
                    text: 'HOME',
                    status: false
                },
                {
                    link: '#',
                    text: 'PAGES',
                    status: true
                },
                {
                    link: '#',
                    text: 'PROGRAM',
                    status: false
                },
                {
                    link: '#',
                    text: 'TICKETS',
                    status: false
                },
                {
                    link: '#',
                    text: 'PAPERS',
                    status: false
                },
                {
                    link: '#',
                    text: 'BLOG',
                    status: false
                },
                {
                    link: '#',
                    text: 'SHORTCODES',
                    status: false
                },
            ]
        }
    }
}
</script>

<template>
    <header class="container d-flex justify-content-between align-items-center h-80px">
        <div>
            <h2><a href="#"> THE KEYNOTE</a></h2>
        </div>
        <ul>
            <HeaderNavBar v-for="(link, index) in links" :key="index" :linkNav="link" />
        </ul>
        <div class="search">
            <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>

        </div>
    </header>
    <section class="jumbotron">
        <div class="container">
            <h1><a href="#">CONFERENCE ON <br>
                    <strong>SOCIAL NETWORKS</strong></a>
            </h1>
            <div class="conference-date my-3">
                <a href="">23-26 MAY 2019 </a> <a href="#"> / SANS FRANCISCO </a> <a href="#"> / 8 SPEAKERS</a>
            </div>
            <div>
                <button class="btn btn-danger my-3">REGISTER ONLINE</button>
            </div>

        </div>
    </section>
    <SectionWhoWeAre />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

header {
    height: 80px;

    h2 {
        font-weight: 900;
    }

    ul,
    .search {
        @include center(both);
        margin: 0.5rem 1rem;

    }

    .fa-solid {
        border-left: solid 1px black;
        padding-left: 2rem;
    }
}


.jumbotron {
    @include center(both);
    text-align: center;
    background-image: url("../assets/slider-1-bg.jpg");
    background-position: center;
    background-size: cover;
    height: 300px;

    a {
        color: white;
    }

    .conference-date a {
        border-top: solid white 2px;
    }
}
</style>