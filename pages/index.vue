<template>
  <div id="page">
    <header id="header">
      <b-container fluid>
        <b-row align-content="center">
          <b-col class="mx-2 px-0"><hr /></b-col>
          <b-col class="col-auto text-center mx-2 px-0">
            <h1>Innovate, Achieve, and Excel with Us</h1>
          </b-col>
          <b-col class="mx-2 px-0"><hr /></b-col>
        </b-row>
        <b-row>
          <b-col class="text-center">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat
              eligendi consectetur voluptatum, laborum ea harum quidem amet.
            </p>
            <button class="btn btn-primary">Consult Now</button>
            <button class="btn btn-outline-primary">Learn More</button>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="text-center">
            <img class="img-fluid" src="~assets/images/header_img.png" alt="" />
          </b-col>
        </b-row>
      </b-container>
    </header>
    <section id="featured">featured</section>
    <section id="about">about</section>
    <section id="practice-areas">practice areas</section>
    <section id="lawyers">lawyers</section>
    <section id="awards">awards</section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.container-fluid {
  min-height: 100vh;
}

#page {
  scroll-snap-type: y mandatory;
}

header,
section,
footer {
  padding: 100px 0;
}

#header {
  background: url('~assets/images/gulapa-mtg-room_img.png');
  margin-top: -180px;
}

#featured {
  height: 2000px;
  background-size: auto 100%;
  background-repeat: no-repeat;
  scroll-snap-align: start;

  hr {
    border: 0;
    border-top: 3px solid $primary;
  }
}

#featured {
  scroll-snap-align: start;
  min-height: 100vh;
}
</style>
