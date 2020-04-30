<template>
  <div class="home">
    <div class="empty"></div>
    <div class="hero-image">
      <div class="hero-text">
        <transition appear name="lol1">
          <h1>Hello, I'm Thibaut</h1>
        </transition>
        <transition appear name="lol2">
          <h2>a full-stack web-developer.</h2>
        </transition>
        <transition appear name="lineFade">
          <hr style="width: 50%; background-color: white " />
        </transition>
        <transition appear name="lol3">
          <router-link to="/about" class="btn btn-light"
            >Find out more</router-link
          >
        </transition>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-image {
  height: 90vh;
  background-image: url("../assets/hero.jpg");
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
  font-weight: bold;
}
h1,
h2 {
  font-size: 4.2rem;
}
h2 {
  font-size: 2.5rem;
}
.btn {
  font-size: 1.4rem;
  background-color: #bc9d47 !important;
}
.btn:hover {
  background-color: #eec45c !important;
}

@media screen and (max-width: 769px) {
  .hero-image {
    height: 95vh;
  }
  h1 {
    font-size: 2.2rem;
  }
  h2 {
    font-size: 1.8rem;
  }
  .btn-light {
    font-size: 1.2rem;
  }
}

.lol1-enter,
.lol2-enter,
.lol3-enter {
  opacity: 0;
  transform: translateY(-50px);
}
.lineFade-enter {
  opacity: 0;
}

.lol1-enter-active {
  transition: opacity 1s ease-in, transform 1s ease;
}
.lol2-enter-active {
  transition: opacity 1s ease-in, transform 1s ease;
  transition-delay: 0.5s;
}
.lineFade-enter-active {
  transition: opacity 1s ease-in, transform 1s ease;
  transition-delay: 1s;
}
.lol3-enter-active {
  transition: opacity 1s ease-in, transform 1s ease;
  transition-delay: 1.5s;
}
</style>
