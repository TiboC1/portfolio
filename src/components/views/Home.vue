<template>
  <div id="home" class="hero-image">
    <div class="hero-text">
      <transition appear name="lol1">
        <h1>Hello, I'm Thibaut</h1>
      </transition>
      <transition appear name="lol2">
        <h2>a full-stack web-developer.</h2>
      </transition>
      <transition appear name="lineFade">
        <hr style="width: 50%; background-color: #eec45c " />
      </transition>
    </div>
    <transition appear name="lol3">
      <div class="hero-icon">
        <a href="#about">
          <svg
            width="40px"
            height="100%"
            viewBox="0 0 247 390"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:1.5;"
          >
            <path
              id="wheel"
              d="M123.359,79.775l0,72.843"
              style="fill:none;stroke:rgb(238,196,92);stroke-width:20px;"
            />
            <path
              id="mouse"
              d="M236.717,123.359c0,-62.565 -50.794,-113.359 -113.358,-113.359c-62.565,0 -113.359,50.794 -113.359,113.359l0,143.237c0,62.565 50.794,113.359 113.359,113.359c62.564,0 113.358,-50.794 113.358,-113.359l0,-143.237Z"
              style="fill:none;stroke:rgb(255,255,255);stroke-width:20px;"
            />
          </svg>
        </a>
      </div>
    </transition>
  </div>
</template>

<style scoped lang="scss">
.hero-image {
  height: 100vh;
  background-image: url("../../assets/hero.jpg");
  background-attachment: fixed;
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
.hero-icon {
  position: absolute;
  top: 90%;
  left: 50%;
  transform: translate(-50%, -90%);
}
h1,
h2 {
  font-size: 4.2rem;
}
h2 {
  font-size: 2.5rem;
}
@keyframes scroll {
  0% {
    transform: translateY(0);
  }
  30% {
    transform: translateY(60px);
  }
}

svg #wheel {
  animation: scroll ease 2s infinite;
}
@media screen and (max-width: 415px) {
  .hero-icon {
    position: absolute;
    top: 85%;
    left: 50%;
    transform: translate(-50%, -85%);
  }
  h1 {
    font-size: 2.2rem;
  }
  h2 {
    font-size: 1.8rem;
  }
}
@media screen and (min-width: 416px) and (max-width: 900px) and (max-height: 767px) {
  .hero-icon {
    position: absolute;
    top: 95%;
    left: 50%;
    transform: translate(-50%, -95%);
  }
  h1 {
    font-size: 2.2rem;
  }
  h2 {
    font-size: 1.8rem;
  }
}
@media screen and (min-width: 415px) and (max-width: 1025px) and (min-height: 767px) and (max-height: 1100px) {
  .hero-icon {
    position: absolute;
    top: 80%;
    left: 50%;
    transform: translate(-50%, -80%);
  }
}

.lol1-enter,
.lol2-enter {
  opacity: 0;
  transform: translateY(-50px);
}
.lol3-enter {
  opacity: 0;
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
  transition: opacity 1s ease-in;
  transition-delay: 1.5s;
}
</style>
