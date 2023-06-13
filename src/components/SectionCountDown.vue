<script>
export default {
    name: 'SectionCountDown',
    data() {
        return {
            countdown: {
                days: 0,
                hours: 0,
                minutes: 0,
                seconds: 0
            },
            targetDate: new Date('May 2, 2024 00:00:00').getTime()
        }
    },
    mounted() {
        setInterval(() => {
            const now = new Date().getTime();
            const distance = this.targetDate - now;

            this.countdown.days = Math.floor(distance / (1000 * 60 * 60 * 24));
            this.countdown.hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.countdown.minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            this.countdown.seconds = Math.floor((distance % (1000 * 60)) / 1000);
        }, 1000);
    }
}
</script>

<template>
    <section class="container-fluid bg_image">
        <div class="container text-center ">
            <div class="row">
                <div class="col-12 d-flex justify-content-center align-items-center">
                    <p>
                    <h2>{{ countdown.days }}</h2> DAYS
                    </p>
                    <p>
                    <h2>{{ countdown.hours }}</h2> HOURS
                    </p>
                    <p>
                    <h2>{{ countdown.minutes }}</h2> MINS
                    </p>
                    <p>
                    <h2>{{ countdown.seconds }}</h2> SECS
                    </p>
                </div>
                <div class="col-12 py-3">
                    <h6>SUBSCRIBE FOR UPDATES</h6>
                </div>
                <div class="col-12 py-5">
                    <form action="">
                        <input class="form-control-lg" type="email" name="" id="" placeholder="Please fill your email">
                        <button class="btn btn-lg btn-danger"> SUBSCRIBE</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

.bg_image {
    background-image: url("/img/coutdown-bg1.jpg");
    background-position: center;
    background-size: cover;

    p {
        padding: 8px 20px;
        color: white;
        background-color: rgba(0, 0, 0, 0.8);
        margin: 30px 10px;
    }
}
</style>