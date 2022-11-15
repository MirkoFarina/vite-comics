<script>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";
import StylizedNavBar from "./components/StylizedNavBar.vue"
export default {
  name: "App",
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
    StylizedNavBar
  },
};
</script>

<template>
    
    <HeaderApp />
    <MainApp />
    <StylizedNavBar />
    <FooterApp />
    
</template>



<style lang="scss">
    @use "./styles/general" as *;
</style>
