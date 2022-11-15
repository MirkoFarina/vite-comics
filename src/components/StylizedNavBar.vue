<script>
export default {
    name: 'StylizedNavBar',
    data (){
        return {
            contentNav: [
                {
                    imgUrl: 'buy-comics-digital-comics.png',
                    text: 'digital comics',
                    current: false
                },
                {
                    imgUrl: 'buy-comics-merchandise.png',
                    text: 'dc merchandise',
                    current: false
                },
                {
                    imgUrl: 'buy-comics-subscriptions.png',
                    text: 'subscription',
                    current: false
                },
                {
                    imgUrl: 'buy-comics-shop-locator.png',
                    text: 'comic shop locator',
                    current: false
                },
                {
                    imgUrl: 'buy-dc-power-visa.svg',
                    text: 'dc power visa',
                    current: false
                }
            ]
        }
    },
    methods: {
        getImagePath(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <nav>
        <div class="container">
            <ul>
                <li
                v-for="(link, index) in contentNav"
                :key="index"
                >
                    <div class="img">
                        <img :src="getImagePath(link.imgUrl)" :alt="link.text">
                    </div>
                    <a href="#">
                        {{link.text}}
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>



<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    nav {
        background-color: $primary-color;
        padding: 20px 0;
        .container {
           ul {
            @include centerFlex('horizontal');
            justify-content: space-around;
            li {
                @include centerFlex;
                width: calc(100% / 5);
                .img {
                    width: 50%;
                    img {
                        transform: scale(.5);
                    } 
                }
                a {
                    font-size: .8rem;
                    color: white;
                    text-transform: uppercase;
                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
           }
            .card {
                color: white;
                
                @include centerFlex('vertical');
                img {
                    transform: scale(.5);
                }
                span {
                    text-transform: uppercase;
                }
            }
        }
    }
</style>