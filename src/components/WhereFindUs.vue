<script>
export default {
    name: 'WhereFindUs'
}
</script>


<template>
    <nav>
        <div class="container">
            <div class="left">
                <a href="#">sing-up now!</a>
            </div>
            <div class="right">
                <span>
                    FOLLOW US
                </span>
                <a href="#">
                    <img src="../assets/img/footer-facebook.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-twitter.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-youtube.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-periscope.png" alt="">
                </a>
            </div>
        </div>
    </nav>
</template>


<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    nav{
        background-color: #303030;
    }
    .container {
        padding: 30px 0;
        @include centerFlex('vertical');
        justify-content: space-between;
    }
    .left {
        a {
            color: white;
            text-transform: uppercase;
            padding: 15px;
            border: 2px solid $primary-color;
            font-weight: 600;
        }
    }
    .right {
        @include centerFlex;
        span {
            color: $primary-color;
            font-weight: 700;
            font-size: 1.2rem;
        }
        img {
            margin-left: 20px;
        }
    }
</style>