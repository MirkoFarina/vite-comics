<script>
import dataCard from "../data/dc-comics";
import CardMain from "./CardMain.vue";
export default {
  name: "MainApp",
  data() {
    return {
      dataCard,
    };
  },
  components: {
    CardMain
  }
};
</script>


<template>
  <main>
    <div class="jumbotron"></div>
    <section>
        <div class="container">
            <h2 class="rectangle">CURRENT SERIES</h2>
            <div class="row">
                <CardMain  
                v-for="(card, index) in dataCard" 
                :key="index" 
                :cardThumb="card.thumb"
                :cardSeries="card.series"
                :cardPrice="card.price"
                />
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


.jumbotron {
  height: 400px;
  background-image: url("../assets/img/jumbotron.jpg");
  background-size: cover;
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