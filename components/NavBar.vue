<template>
  <div>
    <Logo />
    <b-navbar id="navbar" toggleable="lg" type="light" class="bg-white mx-auto">
      <a class="navbar-brand d-lg-none" href="#">
        <Logo />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div id="navbarNavAltMarkup" class="collapse navbar-collapse">
        <div class="navbar-nav flex-lg-grow-1 justify-content-around px-5">
          <a class="nav-item nav-link active" href="/"
            >G-Law<span class="sr-only">(current)</span></a
          >
          <nuxt-link to="/about" class="nav-item nav-link"
            >Who We Are</nuxt-link
          >
          <nuxt-link to="/practice-areas" class="nav-item nav-link"
            >Our Practice Areas</nuxt-link
          >
          <nuxt-link to="/lawyers" class="nav-item nav-link"
            >The Lawyers</nuxt-link
          >
          <nuxt-link to="/awards" class="nav-item nav-link"
            >Gains and Recognitions</nuxt-link
          >
        </div>
      </div>
    </b-navbar>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'NavBar',
})
</script>

<style scoped>
#navbar {
  min-height: 65px;
  border-radius: 10px;
  box-shadow: 0px 4px 12px 0px #07060615;
  font-family: 'montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-weight: 600;
  max-width: 1200px;
  transition: all 0.5s ease;
}
</style>
