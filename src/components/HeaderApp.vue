<script>
export default {
    name: 'HeaderApp'
}
</script>


<template>
    <header>
        <div class="logo">
            <img src="/dc-logo.png" alt="Logo DC">
        </div>
        <nav>
            <ul>
                <li>
                    <a href="#">
                        Characters
                    </a>
                </li>
                <li>
                    <a href="#">
                        Comics
                    </a>
                </li>
                <li>
                    <a class="active" href="#">
                        Movies
                    </a>
                </li>
                <li>
                    <a href="#">
                        tv
                    </a>
                </li>
                <li>
                    <a href="#">
                        games
                    </a>
                </li>
                <li>
                    <a href="#">
                        collectibles
                    </a>
                </li>
                <li>
                    <a href="#">
                        videos
                    </a>
                </li>
                <li>
                    <a href="#">
                        fans
                    </a>
                </li>
                <li>
                    <a href="#">
                        news
                    </a>
                </li>
                <li>
                    <a href="#">
                        shop
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>



<style lang="scss">
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

    header {
        height: 100px;
        @include centerFlex('vertical');
        justify-content: space-between;
        nav {
            height: 100%;
            @include centerFlex;
            ul {
                @include centerFlex('horizzontal');
                li {
                    padding-left: 20px;
                    a {
                        color: #464646;
                        text-transform: uppercase;
                        font-weight: 600;
                        font-size: .9rem;
                        &.active {
                            color: $primary-color;
                        }
                    }
                }
            }
        }
    }
    .logo {
        img{
            width: 80px;
        }
    }
</style>