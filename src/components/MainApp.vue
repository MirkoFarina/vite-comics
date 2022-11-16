<script>
import dataCard from "../data/dc-comics";
export default {
  name: "MainApp",
  data() {
    return {
      dataCard,
    };
  },
};
</script>


<template>
  <main>
    <div class="jumbotron"></div>
    <section>
        <div class="container">
            <h2 class="rectangle">CURRENT SERIES</h2>
            <div class="row">
                <div 
                v-for="(card, index) in dataCard" 
                :key="index" 
                class="card">
                    <div class="top">
                        <img :src="card.thumb" :alt="card.series" />
                        <div class="content">
                            <h5>
                                PREZZO: {{card.price}}
                            </h5>
                        </div>
                    </div>
                    <div class="bottom">
                        <h3>
                            {{ card.series }}
                        </h3>
                    </div>
                </div>
            </div>
        </div>
        <div class="load-more">
            <button class="rectangle">
                LOAD MORE
            </button>
        </div>
    </section>
  </main>
</template>



<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.jumbotron {
  height: 400px;
  background-image: url("../assets/img/jumbotron.jpg");
}

section {
  background-color: #1c1c1c;
  padding-bottom: 40px;
  color: white;
}
.container {
    .rectangle {
        display: inline-block;
        transform: translateY(-50%);
        font-size: 1.4rem;
    }
}

.row {
  display: flex;
  flex-wrap: wrap;
  .card {
    width: calc(100% / 6 - 10px);
    padding: 30px 10px;
    cursor: pointer;
    &:hover .top{
        img {
            transform: scale(1.2);
        }
        .content {
            display: block;
        }
    }
  }
}
.top {
  height: 170px;
  overflow: hidden;
  position: relative;
  img {
    width: 100%;
  }
}

.content {
    background-color: $primary-color;
    position: absolute;
    display: none;
    bottom: 0;
    left: 0;
    padding: 10px 20px;
}
.bottom {
  margin-top: 10px;
  h3  {
    font-size: .9rem;
    font-weight: 400;
  }
}

.load-more {
    text-align: center;
    button {
        cursor: pointer;
        border: none;
        font-weight: 600;
        color: white;
        padding: 10px 50px;
        font-size: .8rem;
    }
}

</style>