<script>
import HeaderNavBar from './HeaderNavBar.vue'
export default {
    name: 'AppHeader',
    components: {
        HeaderNavBar,
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
    <header class="container d-flex ">
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
    <section class="jumbotron d-flex flex-column justife-content-between align-items-center">
        <div class="container">
            <h1><a href="#">CONFERENCE ON <strong>SOCIAL NETWORKS</strong></a></h1>
            <div class="conference-date">
                <a href="">23-26 MAY 2019 </a> <a href="#"> / SANS FRANCISCO </a> <a href="#"> / 8 SPEAKERS</a>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;


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

.jumbotron {
    text-align: center;
    background-image: url("../assets/slider-1-bg.jpg");
    height: 300px;

    a {
        color: white;
    }

    .conference-date a {
        border-top: solid white 2px;
    }
}
</style>