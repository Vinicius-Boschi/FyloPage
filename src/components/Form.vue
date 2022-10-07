<template>
    <div class="main__form">
        <div class="main__form-infos">
            <h1>{{ title }}</h1>
            <p>{{ text }}</p>
            <div class="main__input">
                <input type="email" name="email" id="email" placeholder="Enter your email..." required>
                <button class="main__form-button" type="submit">{{ buttonText }}</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Form',
        data() {
            return {
                title: 'Get early access today',
                text: 'It only takes a minute to sign up and our free starter tier is extremely generous. If you have any questions, our support team would be happy to help you.',
                buttonText: 'Get Started For Free'
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {

        &__form {
            display: flex;
            justify-content: center;
            margin-bottom: -5rem;
        }

        &__form-infos {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            background-color: $DarkBlue;
            border-radius: 10px;
            padding: 2rem;

            h1 {
                font-size: 24px;
            }

            p {
                width: 65%;

                @include phone {
                    width: 100%;
                }
            }   

            @include phone {
                width: 70%;
            }

            @include phone {
                width: 80%;
            }
        }

        &__input {
            display: flex;
            align-items: center;

            @include phone {
                flex-direction: column;
            }
            
            @include tablet {
                flex-direction: column;
            }
        }

        input {
            border-radius: 50px;
            width: 20rem;
            margin-right: 1rem;
            height: 1.5rem;
            padding: 0.3rem;

            &::placeholder {
                padding: 1rem;
            }

            @include phone {
                width: 15rem;
            }
        }

        &__form-button {
            background-color: $Cyan;
            color: $White;
            border-radius: 50px;
            border: none;
            width: 10rem;
            height: 2.5rem;

            @include phone {
                margin-top: 1rem;
            }

            @include tablet {
                margin-top: 1rem;
            }
        }
    }

</style>