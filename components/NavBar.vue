<template>
  <div>
    <b-container class="d-none d-lg-block my-3">
      <b-row>
        <b-col class="text-center">
          <img
            id="logo-text"
            src="~assets/images/logo-text.png"
            alt="logo"
            height="76px"
          />
        </b-col>
      </b-row>
    </b-container>
    <b-navbar
      toggleable="lg"
      type="light"
      class="bg-white mx-auto floating-navbar"
      :class="{ 'sticky-navbar': isSticky }"
    >
      <!-- <a class="navbar-brand d-lg-none" href="#"> </a> -->
      <b-container>
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
          <div
            class="navbar-nav justify-content-around px-5"
            :class="{ 'flex-lg-grow-1': !isSticky }"
          >
            <nuxt-link
              v-for="link in links"
              :key="link.label"
              class="nav-item nav-link"
              :to="link.link"
              >{{ link.label }}</nuxt-link
            >
          </div>
        </div>
      </b-container>
    </b-navbar>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'NavBar',
  data() {
    return {
      links: [
        { label: 'G-Law', link: '/' },
        { label: 'Who We Are', link: '/about' },
        { label: 'Our Practice Areas', link: '/practice-areas' },
        { label: 'The Lawyers', link: '/lawyers' },
        { label: 'Gains and Recognitions', link: '/awards' },
      ],
      isSticky: false,
      stickyClass: 'is_sticky',
      scrollPosition: 0,
    }
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrollPosition = window.scrollY
      if (this.scrollPosition >= 100) {
        this.isSticky = true
      } else {
        this.isSticky = false
      }
    },
  },
})
</script>

<style scoped>
.navbar-nav {
  transition: all 0.5s ease;
}

.floating-navbar {
  min-height: 65px;
  border-radius: 10px;
  box-shadow: 0px 4px 12px 0px #07060615;
  font-family: 'montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-weight: 600;
  max-width: 1200px;
  transition: all 0.5s ease;
}

.floating-navbar:hover {
  max-width: 100%;
}

.sticky-navbar {
  max-width: 100%;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 1030;
  transition: all 0.5s ease;
}
</style>
