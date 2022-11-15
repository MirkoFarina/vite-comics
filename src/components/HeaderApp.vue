<script>
export default {
  name: "HeaderApp",
  data(){
    return {
      navHeader: [
        {
          text: 'characters',
          current: false
        },
        {
          text: 'comics',
          current: true
        },
        {
          text: 'movies',
          current: false
        },
        {
          text: 'tv',
          current: false
        },
        {
          text: 'games',
          current: false
        },
        {
          text: 'collectibles',
          current: false
        },
        {
          text: 'videos',
          current: false
        },
        {
          text: 'fans',
          current: false
        },
        {
          text: 'news',
          current: false
        },
        {
          text: 'shop',
          current: false
        }
      ]
    }
  }
};
</script>


<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="/dc-logo.png" alt="Logo DC" />
      </div>
      <nav>
        <ul>
          <li
          v-for="(link, index) in navHeader"
          :key="index"
          >
            <a 
            :class="{'active' : link.current}" 
            href="#"> 
                {{link.text}} 
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>



<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
  height: 100px;
  @include centerFlex("vertical");
  justify-content: space-between;
  .logo {
    img {
      width: 80px;
    }
  }
  nav {
    height: 100%;
    @include centerFlex;
    ul {
        height: 100%;
        @include centerFlex();
      li {
        height: 100%;
        padding-left: 20px;
        a {
          @include centerFlex();
          height: 100%;
          color: #464646;
          text-transform: uppercase;
          font-weight: 600;
          font-size: 0.9rem;
          height: 100%;
          &.active {
            color: $primary-color;
            border-bottom: 5px solid $primary-color;
            box-shadow: inset -4px -18px 0px -17px $primary-color;
          }
          
        }
      }
    }
  }
}
</style>