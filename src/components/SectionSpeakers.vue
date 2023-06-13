<script>
export default {
    name: 'SectionSpeakers ',
    data() {
        return {
            listSpeakers: [
                {
                    img: '/img/speaker-6-150x150.jpg',
                    name: 'PATRICK SPENCER',
                    task: 'S&P Analyzer',
                },
                {
                    img: '/img/speaker-5-150x150.jpg',
                    name: 'JANET JONES',
                    task: "Newyork Post's GM",
                },
                {
                    img: '/img/speaker-4-150x150.jpg',
                    name: 'MICHAEL DOVER',
                    task: "Starbuck's ceo",
                },
                {
                    img: '/img/speaker-3-150x150.jpg',
                    name: 'ANGELINA HOLY',
                    task: "Maxii's Manager",
                }

            ]

        }
    },
}
</script>

<template>
    <section class="container-fluid bg-light">
        <div class="container ">
            <div class="row py-3">
                <div class="col-12 py-4 text-align-left d-flex justify-content-between align-items-center">
                    <h2>SPEAKERS</h2>
                    <div>
                        <button class="btn btn-danger mx-1"><i class="fa-solid fa-chevron-left"></i></button>
                        <button class="btn btn-danger"><i class="fa-solid fa-chevron-right"></i></button>
                    </div>
                </div>
                <div v-for="speaker in listSpeakers" class="col-3 text-center ">
                    <img :src="speaker.img" :alt="speaker.name">
                    <h6>{{ speaker.name }}</h6>
                    <p>{{ speaker.task }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

h6 {
    padding-top: 1rem;
}

p {
    color: #a3a3a3;
    padding: 1rem 0;
}
</style>