<template>
    <footer class="footer">
        <div class="footer__logo">
            <img :src="logo" :alt="alt">
        </div>
        <div class="footer__content">
            <div class="footer__map">
                <i :class="mapsIcon"></i>
                <p class="footer__text">{{ textMaps }}</p>
            </div>
            <div class="footer__contact">
                <span v-for="info in contact" :key="info.id">
                    <i :class="info.icon"></i>
                    <p>{{ info.textIcon }}</p>
                </span>
            </div>
            <div class="footer__lists">
                <ul class="footer__list">
                    <li class="footer__link" v-for="list in lists" :key="list.id">
                        <a :href="list.link">{{ list.name }}</a>
                    </li>
                </ul>
                <ul class="footer__list">
                    <li class="footer__link" v-for="list in otherList" :key="list.id">
                        <a :href="list.link">{{ list.name }}</a>
                    </li>
                </ul>
            </div>
            <div class="footer__social">
                <ul class="footer__media">
                    <li v-for="item in media" :key="item.id">
                        <a :href="item.link">
                            <i :class="item.icon"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
        data() {
            return {
                logo: 'https://user-images.githubusercontent.com/74377158/194663026-f716b5b5-2370-449a-8e1e-bae4b1854247.svg', alt: 'logo',
                mapsIcon: 'fa-solid fa-location-dot', textMaps: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque, magni suscipit ratione repellendus labore sunt provident. Quasi repudiandae ipsam, quia beatae harum similique unde sint odio eligendi ut cupiditate!',

                contact: [
                    { icon: 'fa-solid fa-phone', textIcon: '+1-543-123-4567' }, 
                    { icon: 'fa-solid fa-envelope', textIcon: 'example@fylo.com' }
                ],
                lists: [ 
                    { link: '#', name: 'About us' }, { link: '#', name: 'Jobs' }, { link: '#', name: 'Press' },
                    { link: '#', name: 'Blog' }
                ],
                otherList: [
                    { link: '#', name: 'Contact us' }, { link: '#', name: 'Terms' }, { link: '#', name: 'Privacy' }
                ],
                media: [
                    { link: '#', icon: 'fa-brands fa-facebook-f' }, { link: '#', icon: 'fa-brands fa-twitter' },
                    { link: '#', icon: 'fa-brands fa-instagram' }
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .footer {
        background-color: $DarkFooter;
        color: $White;
        padding: 2rem;

        &__logo {
            margin-top: 5rem;
        }
        
        &__content {
            display: flex;
            justify-content: space-around;
            align-items: center;

            @include phone {
                flex-direction: column;
            }

            @include tablet {
                flex-direction: column;
            }
        }

        &__map {
            width: 40%;
            display: flex;
            align-items: center;
            
            p {
                margin-left: 1rem;
            }

            @include phone {
                width: 100%;
                margin: 1rem 0 1rem 0;
            }

            @include tablet {
                width: 100%;
                margin: 1rem 0 1rem 0;
            }
        }

        &__text {
            line-height: 1.5;
        }

        &__contact, &__link {
            opacity: .6;
        }

        &__contact {
            line-height: 2;

            span {
                display: flex;
                align-items: center;

                p {
                    margin-left: 1rem;
                }
            }
        }

        &__lists {
            display: flex;
            margin: 1rem;
        }

        &__list {
            margin: 1rem;
            line-height: 2;
        }

        &__link {
            transition: all 1s linear;

            &:hover {
                opacity: 1;
            }
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        &__media {
            display: flex;

            li {
                margin: 1rem;
                border: 1px solid $White;
                border-radius: 50%;
                padding: 1rem;
                transition: 1s;

                &:hover {
                    color: $Cyan;
                }
            }
        }
    }

</style>