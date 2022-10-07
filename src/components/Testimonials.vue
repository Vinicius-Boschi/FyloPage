<template>
    <div class="main__testimonials">
        <img :src="imgQuotes" :alt="altQuotes">
            <div class="main__currency">
                <div class="main__testimonials-content" v-for="item in content" :key="item.id">
                    <h2 class="main__testimonials-title">{{ item.title }}</h2>
                    <div class="main__infos-people">
                        <img class="main__people" :src="item.img" :alt="item.name">
                        <span>
                            <h1>{{ item.name }}</h1>
                            <p>{{ item.job }}</p>
                        </span>
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
    export default {
        name: 'Testimonials',
        data() {
            return {
                imgQuotes: 'https://user-images.githubusercontent.com/74377158/194662978-9b4a8416-8ed5-4b16-96e3-c0e252563d8c.png', altQuotes: 'quotes',
                content: [
                    {
                        title: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.', img: 'https://user-images.githubusercontent.com/74377158/194663031-09f94ff2-ff25-4300-92aa-a5f77e49692e.jpg', name: 'Satish Patel', job: 'Founder & CEO'
                    },
                    {
                        title: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.', img: 'https://user-images.githubusercontent.com/74377158/194663036-80785159-13f6-458d-bc3b-6474d32d90a4.jpg', name: 'Bruce McKenzie', job: 'Founder & CEO'
                    },
                    {
                        title: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.', img: 'https://user-images.githubusercontent.com/74377158/194663040-c28d948b-e8ab-411e-b269-68faf022394a.jpg', name: 'Iva Boyd', job: 'Founder & CEO'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {

        &__testimonials {
            padding: 3rem;
        }

        &__currency {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;

            @include phone {
                grid-template-columns: repeat(1, 1fr);
            }

            @include tablet {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        &__testimonials-content {
            background-color: $DarkTestimonials;
            padding: 1rem;
            border-radius: 10px;
            margin-top: -.5rem;
        }

        &__testimonials-title {
            font-size: 18px;
            line-height: 1.5;
            opacity: .8;
        }

        &__infos-people {
            margin-top: 1rem;
            display: flex;
            align-items: center;

            span {
                padding: .5rem;

                h1 {
                    font-size: 15px;
                }

                p {
                    font-size: 10px;
                }
            }
        }

        &__people {
            border-radius: 50%;
            width: 10%;
        }
    }

</style>