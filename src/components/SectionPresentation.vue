<script>
export default {
    name: 'SectionPresentation',
    data() {
        return {
            listTwitter: [
                {
                    icon: 'fa-brands fa-twitter',
                    date: '3 days ago',
                    text: "Stand out and be vibrant with some the best bright and bold templates on @Envato Elements. And add a splash of c...",

                    link: 'https://t.co/jFrsnzEJK7',
                },
                {
                    icon: 'fa-brands fa-twitter',
                    date: '9 days ago',
                    text: "Stand out and be vibrant with some the best bright and bold templates on @Envato Elements. And add a splash of c...",
                    link: 'Rhttps://t.co/jFrsnzEJK7',
                },
                {
                    icon: 'fa-brands fa-twitter',
                    date: '11 days ago',
                    text: 'Stand out and be vibrant with some the best bright and bold templates on @Envato Elements. And ad splash of c...',
                    link: 'https://t.co/jFrsnzEJK7',
                },

            ],
        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container">
            <div class="row ">
                <div class="col-6 ">
                    <h3>PRESENTATION</h3>
                    <iframe width="480" height="340" src="https://www.youtube.com/embed/JLoFKwMn520"
                        title="YouTube video player" frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                        allowfullscreen></iframe>
                </div>
                <div class="col-6  ">
                    <h3 class="text-center">TWITTER FEED</h3>

                    <div v-for="tweet in listTwitter" class="d-flex align-items-baseline text-left ">
                        <span><i :class="tweet.icon"></i></span>
                        <div>
                            <p>{{ tweet.text }}
                                <a :href="tweet.link">{{ tweet.link }}</a>
                            </p>

                            <p>{{ tweet.date }}</p>
                        </div>

                    </div>

                </div>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

h3 {
    padding: 2rem 0;
    font-weight: 600;
}

div {

    p {
        color: #8d9093;
        padding: 0.5rem 0;

        a {
            color: red;
        }
    }

    i {
        padding-right: 0.5rem;
        color: #47bdee;
    }

}
</style>