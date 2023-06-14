<script>
export default {
    name: 'SectionPresentation',
    data() {
        return {
        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container">
            <div class="row text-center">
                <div class="col-6 ">
                    <h2>PRESENTATION</h2>
                    <iframe width="320" height="240" src="https://www.youtube.com/embed/JLoFKwMn520"
                        title="YouTube video player" frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                        allowfullscreen></iframe>
                </div>
                <div class="col-6 ">
                    <h2>TWITTER FEED</h2>
                    <p></p>

                </div>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

h2 {
    padding: 2rem 0;
}
</style>