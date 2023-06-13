<script>
export default {
    name: 'SectionLocation',
    data() {
        return {
        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container text-center py-5">
            <h2>LOCATION</h2>
            <h4>GB BUILDING, GRAND CONFERENCE ROOM</h4>
            <p><i class="fa-solid fa-location-arrow"></i> 11 GD Building, River Mall, New york,USA 8879</p>
            <p><a style="color: red;" href="#">Check For Accommodations Here</a></p>
            <p><a href="#"> <i class="fa-solid fa-phone"></i> +1-112-2222-3344 <i
                        class="fa-solid fa-envelope"></i>Contact@TheKeynoteTherme.com</a></p>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-image: url("/img/location-bg.jpg");
    background-position: center;
    background-size: cover;
    color: white;

    div {


        a {
            color: white;
        }

        i {
            padding: 0 1rem;
        }

    }

    p,
    h4,
    h2 {
        padding: 1rem 0;
    }

    a {
        border-top: solid 2px white;
        padding: 0.5rem 0;
        color: red;

    }
}
</style>