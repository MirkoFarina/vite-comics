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
          current: false
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
            <a href="#"> {{link.text}} </a>
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
      @include centerFlex("horizzontal");
      li {
        padding-left: 20px;
        a {
          color: #464646;
          text-transform: uppercase;
          font-weight: 600;
          font-size: 0.9rem;
          &.active {
            color: $primary-color;
          }
        }
      }
    }
  }
}
</style>