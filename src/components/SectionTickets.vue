<script>
export default {
    name: 'SectionTickets',
    data() {
        return {
            listTickets: [
                {
                    title: 'ONE DAY PASS',
                    price: 'FREE',
                    listOffered: [

                        'Two Day Access',
                        'Coffee Break',
                        'Lunch(International Buffet)',
                        'Document Sheets',
                        '70USD Voucher For Next Event',
                    ],
                    link: 'BOOK NOW',
                },
                {
                    title: 'ONE DAY PASS',
                    price: 'FREE',
                    listOffered: [

                        'Two Day Access',
                        'Coffee Break',
                        'Lunch(International Buffet)',
                        'Document Sheets',
                        '70USD Voucher For Next Event',
                    ],
                    link: 'BOOK NOW',
                },
                {
                    title: 'ONE DAY PASS',
                    price: 'FREE',
                    listOffered: [

                        'Two Day Access',
                        'Coffee Break',
                        'Lunch(International Buffet)',
                        'Document Sheets',
                        '70USD Voucher For Next Event',
                    ],
                    link: 'BOOK NOW',
                },

            ],

        }
    }
}
</script>

<template>
    <section class="container-fluid">
        <div class="container">
            <div class="py-4  text-center">
                <h2>Tickets</h2>
            </div>

            <div class="row py-3">
                <div class=" col-4  text-center " v-for="ticket in listTickets">
                    <div class="bg_header">
                        <h4>{{ ticket.title }}</h4>
                        <a href="#">{{ ticket.price }}</a>
                    </div>
                    <div class="bg_body">
                        <p v-for="offered in ticket.listOffered">{{ offered }}</p>
                    </div>
                    <div class=" bg_book_now">
                        <a href="#">{{ ticket.link }}</a>
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

section {
    background-image: url("/img/ticket-bg.jpg");
    background-position: center;
    background-size: cover;

    .bg_body {
        background-color: white;
    }

    .bg_header {
        background-color: #e9e9e9;
        padding: 1rem 05rem;
    }

    .bg_book_now {
        background-color: #f62b0a;
        padding: 2rem;

        a {
            color: white;
        }
    }

    h2 {
        color: white;
    }

    h4,
    h2 {
        font-weight: 600;
        padding-bottom: 1rem;
    }

    p {
        padding-bottom: 1rem;
        color: #908787;

    }

    a {
        color: red;
        padding: 1rem 0;
        font-weight: 600;
    }
}
</style>