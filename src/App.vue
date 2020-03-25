<template>
  <div id="app">
  <TheNav></TheNav>
  <transition name="slide" mode="out-in">
    <router-view />
  </transition>
  </div>
</template>

<script>
import TheNav from "@/components/shared/TheNav.vue";

export default {
  components: {
    TheNav
  }
}
</script>


<style>
#app {
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
