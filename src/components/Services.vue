<template>
    <div class="main__services">
        <div class="main__infos" v-for="item in items" :key="item.id">
            <img :src="item.img" :alt="item.alt">
            <h1>{{ item.title }}</h1>
            <p>{{ item.text }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Services',
        data() {
            return {
                items: [
                    {
                        img: 'https://user-images.githubusercontent.com/74377158/194663000-cd34d993-5c38-484e-b30f-ccfa53f279f0.svg', title: 'Access your files, anywhere', text: 'The ability to use a smartphone, tablet, or computer to access your account means your files follow you everywhere.', alt: 'access anywhere'
                    },
                    {
                        img: 'https://user-images.githubusercontent.com/74377158/194663012-e6d16d8b-b37a-4316-ae11-92bffa59c3eb.svg', title: 'Security you can trust', text: '2-factor authentication and user-controlled encryption are just a couple of the security features we allow to help secure your files.', alt: 'security'
                    },
                    {
                        img: 'https://user-images.githubusercontent.com/74377158/194663007-5e14059e-fed3-4f23-bb99-f9121c2ce983.svg', title: 'Real-time collaboration', text: 'Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.', alt: 'collaboration'
                    },
                    {
                        img: 'https://user-images.githubusercontent.com/74377158/194663001-ebcdbe34-710a-45c5-b296-dc3568edc9dd.svg', title: 'Store any type of file', text: 'Wheter you are sharing hollidays photos or work documents, Fylo has you covered allowing for all fille types to be securely stored and shared.', alt: 'any file'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {

        &__services {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            margin-top: 3rem;
            gap: 2rem;

            @include phone {
                grid-template-columns: repeat(1, 1fr);
            }
        }

        &__infos {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            
            h1 {
                margin-top: 1rem;
                margin-bottom: 1rem;
            }

            p {
                width: 40%;

                @include phone {
                    width: 80%;
                }

                @include tablet {
                    width: 80%;
                }
            }
        }
    }

</style>