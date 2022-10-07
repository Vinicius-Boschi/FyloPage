<template>
    <header class="header">
        <div class="header__logo">
            <img :src="logo" :alt="name">
        </div>
        <div class="header__info">
            <ul class="header__list">
                <li v-for="item in list" :key="item.id">
                    <a :href="item.link">{{ item.name }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return {
                logo: 'https://user-images.githubusercontent.com/74377158/194663026-f716b5b5-2370-449a-8e1e-bae4b1854247.svg', name: 'logo',
                list: [
                    { name: 'Features', link: '#'}, { name: 'Team', link: '#'}, { name: 'Sign In', link: '#'}
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .header {
        background-color: $DarkBlue;
        color: $White;
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 3rem;
        font-family: $fontRaleway;

        &__logo {

            img {
                @include phone {
                    width: 6rem;
                }
            }
        }

        &__list {
            display: flex;
            align-items: center;

            li {
                padding: 1rem;
            }

            a {
                text-decoration: none;
                color: inherit;
                cursor: pointer;
                opacity: .5;
                transition: 1s;

                &:hover {
                    opacity: 1;
                    text-decoration: underline;
                }
            }
        }
    }
</style>