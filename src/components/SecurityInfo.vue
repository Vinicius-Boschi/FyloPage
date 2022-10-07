<template>
    <div class="main__content">
        <div class="main__picture">
            <img class="main__image" src="https://user-images.githubusercontent.com/74377158/194663018-7eb7fb92-5ae8-420d-9a2e-2e61f72ff2b5.png" alt="intro">
        </div>
        <div class="main__texts">
            <h1 class="main__title">{{ title }}</h1>
            <p class="main__text">{{ text }}</p>
            <button class="main__button">{{ textButton }}</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'SecurityInfo',
        data() {
            return {
                title: 'All your files in one secure location, accessible anywhere.',
                text: 'Fylo stores all your most important files in one securite location, Accessible them wherever you need, share and collaborate with friends family, and co-workers.',
                textButton: 'Get Started'
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {
        color: $White;

        &__content {
            background-color: $DarkBlue;
            text-align: center;
        }

        &__image {
            width: 40%;
        }

        &__texts {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        h1 {
            font-size: 20px;
            font-weight: bold;
            line-height: 1.5;
            font-family: $fontRaleway;
        }

        p {
            margin-top: 1rem;
            margin-bottom: 1rem;
            line-height: 1.5;
            font-size: 12px;
            opacity: .8;
        }

        &__title {
            width: 30%;

            @include phone {
                width: 100%;
            }

            @include tablet {
                width: 60%;
            }
        }

        &__text {
            width: 25%;

            @include phone {
                width: 100%;
            }

            @include tablet {
                width: 50%;
            }
        }

        &__button {
            background-color: $Blue;
            color: $White;
            border: none;
            border-radius: 1rem;
            cursor: pointer;
            width: 10rem;
            height: 2rem;
            margin-bottom: 2rem;
        }
    }

</style>