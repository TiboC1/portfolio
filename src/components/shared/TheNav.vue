<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark navbar-shrink fixed-top">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo03" aria-controls="navbarTogglerDemo03" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
            <ul class="navbar-nav ml-auto mt-2 mt-lg-0">
                <li class="nav-item">
                    <router-link to="/" class="nav-link">Home</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/about" class="nav-link">About</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/about" class="nav-link">Portfolio</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/contact" class="nav-link">Contact</router-link>
                </li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>
    nav{
        font-size: 2em;
        min-height: 8vh;
    }
    .nav-link{
        color: white !important;

    }


    @media only screen and (min-width: 991px) {
        nav{
        background-color:transparent !important;
        font-size: 1.5em;
        }
    }
</style>