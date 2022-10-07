<template>
    <div class="main__infos-productive">
        <div class="main__productive">
            <img :src="img" :alt="alt">
        </div>
        <div class="main__about">
            <h1>{{ title }}</h1>
            <p>{{ text }}</p>
            <p>{{ textTwo }}</p>
            <span>
                <a :href="link">{{ textLink }}</a>
            </span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Productive',
        data() {
            return {
                img: 'https://user-images.githubusercontent.com/74377158/194663023-9cc3ab0e-f7db-40ea-a334-8aa3f47f0e4b.png',
                alt: 'productive img',
                title: 'Stay productive, wherever you are.',
                text: 'Never let location be an issue when accessing your files. Fylo has you covered for all of your file storage needs.',
                textTwo: 'Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.',
                link: '#', textLink: 'See how Fylo works'
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {

        &__infos-productive {
            display: flex;
            align-items: center;
            justify-content: center;

            @include phone {
                flex-wrap: wrap;
            }

            @include tablet {
                flex-wrap: wrap;
            }
        }

        &__productive {
            padding: 3rem;

            img {
                width: 90%;
            }
        }

        &__about {

            @include phone {
                display: flex;
                flex-direction: column;
                align-items: center;
            }

            @include tablet {
                display: flex;
                flex-direction: column;
                align-items: center;
            }

            p {
                width: 62%; 

                @include phone {
                    width: 75%;
                }
            }
        }

        a {
            text-decoration: none;
            color: inherit;

            &:hover {
                text-decoration: underline;
                color: $Cyan;
            }
        }
    }

</style>    