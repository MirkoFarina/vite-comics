<script>
import StylizedNavBar from "./StylizedNavBar.vue";
import WhereFindUs from "./WhereFindUs.vue";
import { navDc, navDcComics, navShop, navSites} from "../data/nav-footer";
export default {
    name:'FooterApp',
    components: {
        StylizedNavBar,
        WhereFindUs
    },
    data (){
        return {
            navDc,
            navDcComics,
            navShop,
            navSites
        }
    }
}
</script>


<template>
    <StylizedNavBar />
    <footer>
        <div class="container">
            <div class="col">
                <nav>
                    <h4>
                        dc comics
                    </h4>
                    <ul>
                        <li 
                        v-for="(item, index) in navDcComics"
                        :key="index"
                        >
                            <a :href="item.href">{{item.text}}</a>
                        </li>
                    </ul>
                </nav>
                <nav>
                    <h4>
                        shop
                    </h4>
                    <ul>
                        <li
                        v-for="(item, index) in navShop"
                        :key="index"
                        >
                            <a :href="item.href">{{item.text}}</a>
                        </li>
                    </ul>
                </nav>
            </div>
            <div class="col">
                <nav>
                    <h4>
                        dc
                    </h4>
                    <ul>
                        <li
                        v-for="(item, index) in navDc"
                        :key="index"
                        >
                            <a :href="item.href">
                                {{item.text}}
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
            <div class="col">
                <nav>
                    <h4>
                        sites
                    </h4>
                    <ul>
                        <li
                        v-for="(item, index) in navSites"
                        :key="index"
                        >
                            <a :href="item.href">{{item.text}}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <div class="background-layer">
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </footer>
    <WhereFindUs />
</template>



<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    footer {
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        padding: 25px 0;
        overflow: hidden;
        position: relative;
    }
    .container {
        @include centerFlex('vertical');
        align-items: flex-start;
        h4 {
            text-transform: uppercase;
            font-weight: 800;
            color: white;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        ul {
            margin-bottom: 30px;
        }
        li {
            margin: 5px 0;
            a {
                color: #959595;
                font-size: .8rem;
                &:hover {
                        text-decoration: underline;
                    }
            }
        }
    }
    .col {
        margin-left: 30px;
        &:first-of-type {
            margin: 0;
        }
    }
    .background-layer {
        position: absolute;
        top: -70px;
        right: 20%;
    }
</style>