<script>
export default {
    name: 'SectionFooterBottom',
    data() {
        return {
        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container d-flex justify-content-between con align-items-center">
            <div>
                <a href="#">@ Copyright GoodLayers,All Right Reserved</a>
            </div>
            <div>
                <a href="#">About us / Accommodation / Call For Paper / Contact Us</a>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: #222222;

    .container {
        height: 60px
    }

    a {
        color: #868178;
    }
}
</style>