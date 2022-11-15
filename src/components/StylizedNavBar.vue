<script>
export default {
    name: 'StylizedNavBar'
}
</script>

<template>
    <nav>
        <div class="container">
            <div class="card">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                <span>
                    DIGITAL COMICS
                </span>
            </div>
            <div class="card">
                <img src="../assets/img/buy-comics-merchandise.png" alt="">
                <span>
                    DC Merchandise
                </span>
            </div>
            <div class="card">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                <span>
                   subscription
                </span>
            </div>
            <div class="card">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                <span>
                    comic shop locator
                </span>
            </div>
            <div class="card">
                <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                <span>
                    dc power visa 
                </span>
            </div>
        </div>
    </nav>
</template>



<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    nav {
        background-color: $primary-color;
        padding: 50px 0;
        .container {
            @include centerFlex('horizontal');
            justify-content: space-between;
            .card {
                color: white;
                @include centerFlex();
                img {
                    width: 50px;
                }
                span {
                    padding-left: 10px;
                    text-transform: uppercase;
                }
            }
        }
    }
</style>