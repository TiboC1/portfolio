<template>
  <div id="app">
    <TheNav></TheNav>
    <transition name="fade">
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
  height: 100vh;
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: black;
}

.fade-enter-active,
.fade-leave-active{
  transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to{
  opacity: 0;
}

</style>
