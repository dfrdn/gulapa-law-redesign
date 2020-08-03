<template>
  <div id="header">
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
      <b-container>
        <transition name="fade">
          <b-navbar-brand
            class="order-1 order-lg-0"
            :class="{ 'd-lg-none': !isSticky }"
            to="/"
          >
            <img
              id="logo-figure"
              src="~assets/images/logo-figure.png"
              alt="logo"
              height="40px"
            />
          </b-navbar-brand>
        </transition>
        <b-navbar-toggle
          class="order-0 order-lg-1"
          type="button"
          target="nav-collapse"
        >
          <!-- <span class="navbar-toggler-icon"></span> -->
        </b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav class="order-2 order-lg-0">
          <b-navbar-nav
            class="justify-content-around px-5 order-2"
            :class="{ 'flex-lg-grow-1': !isSticky }"
          >
            <nuxt-link v-if="!isSticky" class="nav-item nav-link mx-3" to="/"
              >G-Law</nuxt-link
            >

            <nuxt-link
              v-for="link in stickyLinks"
              :key="link.label"
              class="nav-item nav-link mx-3"
              :to="link.link"
              >{{ link.label }}</nuxt-link
            >
          </b-navbar-nav>
        </b-collapse>
        <transition name="fade">
          <b-button
            class="d-none"
            :class="[!isSticky && isHome ? 'd-lg-none' : 'd-lg-block']"
            variant="primary"
            to="/contact"
            >Consult Us</b-button
          >
        </transition>
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
      stickyLinks: [
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
  computed: {
    isHome() {
      return (
        this.$nuxt.$route.name === 'index' ||
        this.$nuxt.$route.name === 'contact'
      )
    },
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      const width =
        window.innerWidth > 0
          ? window.innerWidth
          : document.documentElement.clientWidth
      this.scrollPosition = window.scrollY
      if (width < 992) {
        this.isSticky = true
      } else if (this.scrollPosition >= 130) {
        this.isSticky = true
      } else {
        this.isSticky = false
      }
    },
  },
})
</script>

<style lang="scss" scoped>
#header {
  height: 150px;
  @media (max-width: 992px) {
    height: 80px;
  }
}

.navbar-nav {
  transition: flex 0.3s ease;
}

a {
  transition: all 0.3s ease;
}

.spacer {
  height: 140px;
  /* background: black; */
}

.floating-navbar {
  min-height: 65px;
  border-radius: 10px;
  box-shadow: 0px 4px 12px 0px #07060615;
  font-family: 'montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-weight: 600;
  max-width: 1200px;
  transition: all 0.3s ease;
}

.sticky-navbar {
  max-width: 100%;
  width: 100%;
  position: fixed;
  border-radius: 0;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1030;
  transition: all 0.3s ease;
}

.nuxt-link-exact-active {
  color: $accent !important;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}

#logo-figure {
  margin-left: -2px;
}

.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  transition-delay: 0;
  transform: translateX(10px);
  opacity: 0;
}
</style>
