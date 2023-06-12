<script>
export default {
    name: 'SectionFooterTop',
    data() {
        return {
            listData: [
                {
                    link: '#',
                    text: 'SEM PORTA MOLLIS PARTURIENT',
                },
                {
                    link: '#',
                    text: 'NULLAM LOREM MATTIS PURUS',
                },
                {
                    link: '#',
                    text: 'SEM PORTA MOLLIS PARTURIENT',
                },
                {
                    link: '#',
                    text: 'NULLAM LOREM MATTIS PURUS',
                },
                {
                    link: '#',
                    text: 'SEM PORTA MOLLIS PARTURIENT',
                },
            ],
            listImg: [
                {
                    link: '#',
                    img: '/img/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-6745585-modern-creative-workspace-m-150x150.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8522811-speaker-at-business-conference-and-present (1).jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8523683-speaker-at-business-convention-and-present.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8795110-overhead-of-essentials-denim-clothes-m-150.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8523683-speaker-at-business-convention-and-present.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-6745585-modern-creative-workspace-m-150x150.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg',
                },
                {
                    link: '#',
                    img: '/img/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg',
                },
            ]
        }
    }
}
</script>

<template>
    <section class="container-fluid bg-dark">
        <div class="container py-2">
            <div class="row">
                <div class="col-3">
                    <h5><a href="#"> ABOUT US</a></h5>
                    <p>Laudantium inventore necessitatibus, praesentium omnis temporibus vel debitis.</p>
                    <div class="icon">
                        <ul>
                            <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a></li>
                            <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
                            <li><a href="#"><i class="fa-brands fa-linkedin-in"></i></a></li>
                            <li><a href="#"><i class="fa-brands fa-google-plus-g"></i></a></li>
                            <li><a href="#"><i class="fa-solid fa-p"></i></a></li>
                            <li><a href="#"><i class="fa-brands fa-rocketchat"></i></a></li>
                        </ul>
                    </div>
                </div>

                <div class="col-3">
                    <h5><a href="#">RECENT NEWS</a></h5>
                    <div>
                        <ul>
                            <li v-for="data in listData "><a :href="data.link"> <i class="fa-solid fa-caret-right"></i> {{
                                data.text }}</a></li>
                        </ul>
                    </div>
                </div>

                <div class="col-3">
                    <h5><a href="#"> GET YOUR SEAT!</a></h5>
                    <p>Book for your seat before it's too rate. We provide variety of ticket options.</p>
                    <div>
                        <button class="btn btn-danger my-3">CHECK OUT TICKETS!</button>
                    </div>
                </div>

                <div class="col-3">
                    <h5><a href="#"> GALLERY FROM LAST YEAR</a></h5>
                    <ul class="d-flex flex-wrap">
                        <li class="container_img py-1 px-1" v-for="img in listImg"><a :href="img.link"><img :src="img.img"
                                    alt=""></a>
                        </li>
                    </ul>
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

    .container_img {
        width: calc(100% / 4);
    }


    .icon {
        padding: 2rem 0;

        ul {
            @include center(both);
            margin: 0.5rem 1rem;

            a {
                color: #78746b;
                background-color: white;
                padding: 5px 5px;
                border-radius: 25%;
            }


        }
    }

    p,
    a {
        color: #78746b;
        font-size: 12px;
    }

    h5 {
        padding: 2rem 0;

        a {
            color: white;

        }
    }
}
</style>