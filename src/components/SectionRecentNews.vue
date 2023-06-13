<script>
export default {
    name: 'SectionRecentNews',
    data() {
        return {
            listData: [
                {
                    img: '/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (2).jpg',
                    date: '03 dec 2013  /  0 Comments',
                    title: 'INVENTORE NECESSITATIBUS',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Read More',
                },
                {
                    img: '/img/photodune-8797753-multiethnic-people-with-startup-business-t (2).jpg',
                    date: '03 dec 2013  /  0 Comments',
                    title: 'MAGNA PARS STUDIORUM',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Read More',
                },
                {
                    img: '/img/photodune-8522811-speaker-at-business-conference-and-present (2).jpg',
                    date: '03 dec 2013  /  0 Comments',
                    title: 'DONEC LUCTUS IMPERDIET',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Read More',
                },
            ],

        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container">
            <div class="row py-3">
                <div class="col-12 py-4  text-center d-flex justify-content-between align-items-center">
                    <h3>Recent News</h3>
                    <a href="#">Read All News</a>
                </div>
                <div class="col-4" v-for="data in listData">
                    <img :src="data.img" :alt="data.title">
                    <div>
                        <p>{{ data.date }}</p>
                        <h5>{{ data.title }}</h5>
                        <p>{{ data.text }}</p>
                        <a href="#">{{ data.link }}</a>
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

.container {
    h5 {
        font-weight: 600;
        padding-bottom: 1rem;
    }

    p {
        padding-bottom: 1rem;
        color: #bababa;

    }

    a {
        color: red;
        padding-top: 2rem;
    }
}
</style>