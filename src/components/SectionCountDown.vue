<script>
export default {
    name: 'SectionCountDown',
    data() {
        return {
            listData: [
                {
                    icon: 'fa-solid fa-trophy',
                    title: 'WHO WE ARE',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Learn More',
                },
                {
                    icon: 'fa-solid fa-bolt-lightning',
                    title: 'WHAT WE DO',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Learn More',
                },
                {
                    icon: '<fa-solid fa-question',
                    title: 'WHY US',
                    text: 'Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis',
                    link: 'Learn More',
                },
            ],

        }
    }
}
</script>

<template>
    <div class="container">
        <div class="d-flex" v-for="data in listData">
            <i :class="data.icon"></i>
            <div>
                <h5>{{ data.title }}</h5>
                <p>{{ data.text }}</p>
                <a href="#">{{ data.link }}</a>
            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

.container {
    @include center(both);
    height: 200px;

    h5 {
        font-weight: 600;
        padding-bottom: 1rem;
    }

    p {
        padding-bottom: 1rem;
        color: #bababa;

    }

    i {
        color: #bababa;
        font-size: 20px;
        padding: 0.5rem 1rem;
    }

    a {
        color: red;
        padding-top: 2rem;
    }
}
</style>