<template>
  <nav
    id="navbar"
    class="navbar navbar-expand-lg navbar-light bg-light navbar-shrink nav sticky-top"
  >
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarToggler"
      aria-controls="navbarToggler"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarToggler">
      <ul class="navbar-nav ml-auto mt-lg-0">
        <li class="nav-item">
          <a href="#home" class="nav-link nav-link-active">Home</a>
        </li>
        <li class="nav-item">
          <a href="#about" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a href="#portfolio" class="nav-link">Portfolio</a>
        </li>
        <li class="nav-item">
          <a href="#contact" class="nav-link">Contact</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script></script>

<style scoped>
nav {
  font-size: 1.5rem;
  font-weight: bold;
}
.active {
  color: #fdd947 !important;
}
</style>
