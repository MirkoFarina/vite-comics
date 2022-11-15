<script>
export default {
    name:'FooterApp'
}
</script>


<template>
    <footer>
        <div class="container">
            <div class="col">
                <nav>
                    <h4>
                        dc comics
                    </h4>
                    <ul>
                        <li>
                            <a href="#">Characters</a>
                        </li>
                        <li>
                            <a href="#">Comics</a>
                        </li>
                        <li>
                            <a href="#">Movies</a>
                        </li>
                        <li>
                            <a href="#">TV</a>
                        </li>
                        <li>
                            <a href="#">Games</a>
                        </li>
                        <li>
                            <a href="#">Videos</a>
                        </li>
                        <li>
                            <a href="#">News</a>
                        </li>
                    </ul>
                </nav>
                <nav>
                    <h4>
                        shop
                    </h4>
                    <ul>
                        <li>
                            <a href="#">Shop DC</a>
                        </li>
                        <li>
                            <a href="#">Shop DC Collectibles</a>
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
                        <li>
                            <a href="#">
                                Terms Of Use
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Privacy policy (New)
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Ad Choices
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Advertising
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Jobs
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Subscriptions
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Talent Workshops
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                CPSC Certificates
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Ratings
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Shop Help
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Contact Us
                            </a>
                        </li>
                -
                    </ul>
                </nav>
            </div>
            <div class="col">
                <nav>
                    <h4>
                        sites
                    </h4>
                    <ul>
                        <li>
                            <a href="#">DC</a>
                        </li>
                        <li>
                            <a href="#">MAD Magazine</a>
                        </li>
                        <li>
                            <a href="#">DC Kids</a>
                        </li>
                        <li>
                            <a href="#">DC Universe</a>
                        </li>
                        <li>
                            <a href="#">DC Power Visa</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <div class="background-layer">
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </footer>
</template>



<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    footer {
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        padding: 30px 0;
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