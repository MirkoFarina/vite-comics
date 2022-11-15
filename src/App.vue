<script>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";
import StylizedNavBar from "./components/StylizedNavBar.vue";
import WhereFindUs from "./components/WhereFindUs.vue";
export default {
  name: "App",
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
    StylizedNavBar,
    WhereFindUs
  },
};
</script>

<template>
    
    <HeaderApp />
    <MainApp />
    <StylizedNavBar />
    <FooterApp />
    <WhereFindUs />
</template>



<style lang="scss">
    @use "./styles/general" as *;
</style>
