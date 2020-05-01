<template>
  <div id="app">
    <AppHome />
    <AppNav />
    <AppAbout />
    <AppPortfolio />
    <AppContact />
    <AppFooter />
  </div>
</template>

<script>
import AppNav from "@/components/shared/TheNav.vue";
import AppFooter from "@/components/shared/TheFooter.vue";
import AppHome from "@/components/views/Home.vue";
import AppAbout from "@/components/views/About.vue";
import AppPortfolio from "@/components/views/Portfolio.vue";
import AppContact from "@/components/views/Contact.vue";

export default {
  components: {
    AppNav,
    AppFooter,
    AppHome,
    AppAbout,
    AppPortfolio,
    AppContact
  }
};
</script>

<style>
html {
  overflow-x: hidden;
  scroll-behavior: smooth !important;
}
#app {
  font-family: "Cormorant Upright", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.empty {
  height: 70px;
}
@media screen and (max-width: 980px) {
  .empty {
    height: 50px;
  }
}
</style>
