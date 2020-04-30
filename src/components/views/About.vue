<template>
  <div class="about">
    <div class="empty"></div>
    <div class="container">
      <h2 class="mt-4 h1" style="font-weight: bold">About Me</h2>
      <div class="row intro">
        <h3 class="mx-auto my-3 h2">Who am I?</h3>
        <p>
          I am a junior web-developer with a passion for making things work and
          look beautiful. I started learning in october 2019 after trying out
          many other career paths. Why settle for web-development you ask?
          Because it is a a perfect combination of making things functional and
          being creative. I graduated with a bachelor of arts in history and
          theology.
        </p>
        <div class="mx-auto">
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
              style="fill:none;stroke:rgba(0,0,0,0.6);stroke-width:20px;"
            />
            <path
              id="mouse"
              d="M236.717,123.359c0,-62.565 -50.794,-113.359 -113.358,-113.359c-62.565,0 -113.359,50.794 -113.359,113.359l0,143.237c0,62.565 50.794,113.359 113.359,113.359c62.564,0 113.358,-50.794 113.358,-113.359l0,-143.237Z"
              style="fill:none;stroke:rgba(0,0,0,0.61);stroke-width:20px;"
            />
          </svg>
        </div>
      </div>
    </div>
    <div id="main-icons" class="container-fluid">
      <h3 class="h2">
        My 4 top priorities:
      </h3>
      <transition appear name="fadeLeft">
        <div class="col-md-4 my-4 offset-md-2">
          <img src="../assets/speed.png" alt="" class="m-2 mx-auto" />
          <h4 class="h2">Fast</h4>
          <p>
            I focus on speed optimization to ensure the user has a great
            experience browsing the site by reducing page load times
          </p>
        </div>
      </transition>

      <div class="col-md-4 my-4 offset-md-6" data-aos="fade-left">
        <img src="../assets/responsive.png" alt="" class="m-2 mx-auto" />
        <h4 class="h2">Responsive</h4>
        <p>
          I always make sure to make the website look good on both desktops and
          mobile devices
        </p>
      </div>
      <div class="col-md-4 my-4 offset-md-2" data-aos="fade-right">
        <img src="../assets/dynamic.png" alt="" class="m-2 mx-auto" />
        <h4 class="h2">Dynamic</h4>
        <p>
          I make sure to build a custom theme built specifically for each
          project
        </p>
      </div>
      <div class="col-md-4 my-4 offset-md-6" data-aos="fade-left">
        <img src="../assets/seo.png" alt="" class="m-2 mx-auto" />
        <h4 class="h2">SEO</h4>
        <p>
          I also aspire to create websites that rank well in search engine
          listings to ensure a high amount of traffic
        </p>
      </div>
    </div>
    <div class="container">
      <h3 class="mt-5">These are the technologies use and am familiar with:</h3>
      <ul class="list-group" data-aos="fade-left">
        <li class="list-item">HTML</li>
        <li class="list-item">CSS</li>
        <li class="list-item">Javascript</li>
        <li class="list-item">Vue</li>
        <li class="list-item">PHP</li>
        <li class="list-item">Laravel</li>
        <li class="list-item">Symfony</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
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
img {
  width: 120px;
}
.about * {
  font-weight: bold;
  color: rgba(0, 0, 0, 0.6);
}
.about {
  font-size: 1.5rem;
  background-color: #f8f9fa;
}
.fadeLeft-enter {
  opacity: 0;
  transform: translateX(-150px);
}
.fadeLeft-enter-active {
  transition: opacity 0.5s ease-in, transform 0.5s ease;
}

  .intro{
    height: 80vh;
  }
</style>
