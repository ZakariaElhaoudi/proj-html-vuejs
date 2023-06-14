<script>
export default {
    name: 'SectionSponsors',
    data() {
        return {
            listSponsors: [
                {
                    img: '/img/banner-1.jpg',
                },
                {
                    img: '/img/banner-2.jpg',
                },
                {
                    img: '/img/banner-3.jpg',
                },
                {
                    img: '/img/banner-4.jpg',
                },
                {
                    img: '/img/banner-5.jpg',
                },
                {
                    img: '/img/banner-6.jpg',
                },
            ],
        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container">
            <div class="row text-center py-5">
                <div class="col-12">
                    <h3>Sponsors</h3>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Perspiciatis sint illum consequatur dolore
                        aliquam soluta! Sint laboriosam inventore in ducimus eos voluptas est, sunt porro accusantium
                        maiores at
                        exercitationem excepturi.</p>
                </div>

                <div v-for="spondorsImg in listSponsors" class="col-2">
                    <img :src="spondorsImg.img" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/general.scss' as *;

section {
    background-color: #f6f6f6;

    h3 {
        padding: 2rem 0;
        font-weight: 600;
    }




    p {
        color: #8d9093;
        padding: 0.5rem 0;

        a {
            color: red;
        }
    }


}
</style>