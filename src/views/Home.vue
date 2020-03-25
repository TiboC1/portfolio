<template>
  <div class="home">
      <div class="hero-image">
          <div class="hero-text">
            <transition appear name="lol1">
              <h1>Hello, I'm Thibaut M.</h1>
            </transition>
            <transition appear name="lol2">
              <h2>and I'm a full-stack web-developer.</h2>
            </transition>
            <transition appear name="lol3">
              <router-link to="/about" class="btn btn-light">Find out more</router-link>
            </transition>
          </div>
      </div>
  </div>
</template>



<style scoped>
  .hero-image {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/hero-image.jpg");
  height: 100vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.hero-text {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}

.lol1-enter, .lol2-enter, .lol3-enter{
  opacity: 0;
  transform: translateY(-50px);
}

.lol1-enter-active{
  transition: opacity 1s ease-in, transform 1s ease;
}

.lol2-enter-active{
  transition: opacity 1s ease-in, transform 1s ease;
  transition-delay: .5s;
}

.lol3-enter-active{
  transition: opacity 1s ease-in, transform 1s ease;
  transition-delay: 1s;
}
</style>

