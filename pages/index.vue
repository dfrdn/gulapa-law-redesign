<template>
  <div>
    <header id="header">
      <b-container>
        header
      </b-container>
    </header>
    <section id="featured">
      featured
    </section>
    <section id="about">
      about
    </section>
    <section id="practice-areas">
      practice areas
    </section>
    <section id="lawyers">
      lawyers
    </section>
    <section id="awards">
      awards
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.container {
  min-height: 100vh;
}

#header {
  background: url('~assets/images/gulapa-mtg-room_img.png');
}
</style>
