<script>
export default {
    name: 'SectionProgram',
    data() {
        return {
            listPrograms: [
                {
                    day: 'DAY 1',
                    date: '23 May 2016',
                    active: true
                },
                {
                    day: 'DAY 2',
                    date: '23 May 2030',
                    active: false
                },
                {
                    day: 'DAY 3',
                    date: '24 May 2030',
                    active: false
                },
                {
                    day: 'DAY 4',
                    date: '25 May 2030',
                    active: false
                },
                {
                    day: 'DAY 5',
                    date: '26 May 2030',
                    active: false
                },
                {
                    day: '',
                    date: '',
                    active: false
                },

            ]

        }
    },
}
</script>

<template>
    <section class="container-fluid bg-light">
        <div class="container ">
            <div class="row py-3">
                <div class="col-12 py-5 d-flex justify-content-between align-items-center">
                    <h2>PROGRAM</h2>
                    <p>This conference run througt all 4 days from 23 - 26 May 2016. <br> We also provide free lunch and
                        coffee
                        break in each day </p>
                    <a href="#">View Full Program</a>
                </div>
                <div v-for="(program, index) in listPrograms" class="col-2 text-center btn_bg"
                    :class="{ btn_bg_active: program.active }">
                    <a href="#">
                        <h5>{{ program.day }}</h5>
                        <p>{{ program.date }}</p>
                    </a>
                </div>
            </div>
            <div class="row data_conference py-3">
                <div class="col-3 py-3">
                    <p> <i class="fa-regular fa-clock"></i> 09:00-10:30</p>
                    <p><i class="fa-solid fa-location-arrow"></i> ROOM A</p>
                    <i class="fa-solid fa-user"></i> <a href="#"> LAURENCE FRANCIS</a>
                </div>
                <div class="col-9 py-3">
                    <h5>WELCOMING AND INTRODUCTION</h5>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vel id adipisci recusandae totam, ipsa
                        ex praesentium, suscipit excepturi corporis omnis.</p>
                    <img src="/img/speaker-3-150x150.jpg" alt="">
                </div>

            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

.btn_bg {
    background-color: #f62b0a;
    color: white;
    padding: 20px 40px;
    border-left: solid 1px #dc2b0d;

    a {
        color: white;
    }

    &:hover,
    :active {
        background-color: #c72b11;
    }
}

.data_conference {
    background-color: #f7f7f7;

    p,
    i {
        color: #a6a8a8;
        padding: 0.5rem;
    }

    a {
        color: #dc2b0d;
    }
}
</style>