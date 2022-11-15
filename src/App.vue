<script>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";
export default {
  name: "App",
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
  },
};
</script>

<template>
    <div class="container">
        <HeaderApp />
        <MainApp />
        <FooterApp />
    </div>
</template>



<style lang="scss">
    @use "./styles/general" as *;
</style>
